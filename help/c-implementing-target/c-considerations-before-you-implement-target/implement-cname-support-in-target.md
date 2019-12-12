---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Information about working with Adobe Client Care to implement CNAME (Canonical Name) support in Adobe Target.
title: CNAME and Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
---

# CNAME and Adobe Target {#cname-and-adobe-target}

Instructions about working with Adobe Client Care to implement CNAME (Canonical Name) support in [!DNL Adobe Target]. To best handle ad blocking issues, or ITP-related cookie policies, a CNAME is used so calls are made to a domain owned by the customer rather than a domain owned by Adobe.

## Request CNAME support

Perform the following steps to request CNAME support in [!DNL Target]:

1. Adobe's certificate authority (DigiCert) needs to verify Adobe is authorized to generate certificates under your domain. 

   DigiCert calls this process [Domain Control Validation](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) (DCV), and Adobe will not be allowed to generate a certificate under your domain until this process is complete. 
   
   DCV uses a few methods, and there a few things you can do before opening an Adobe Client Care ticket (step 3) to help expedite the DCV process:

   * DigiCert will first try the email method, in which they send emails to addresses found in the domain's WHOIS information as well as pre-determined email addresses (admin, administrator, webmaster, hostmaster, and postmaster `@[domain_name]`). See the [DCV methods documentation](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) for more information. 

     To expedite the DCV email process, DigiCert provides the following recommendation:

     "Please verify that your registrar/WHOIS provider has not masked or removed [relevant email addresses]. If they are, find out if they provide a way (e.g., anonymized email address, web form) for you to allow [certificate authorities] to access your domain’s WHOIS data."

   * If the DCV email method is not an option for you, the next method is the DNS TXT method, in which you add a DNS TXT record to your domain with a hash value. This TXT record indicates to DigiCert that Adobe is authorized to generate the certificate. If you need to use this method, let Adobe Client Care know when you open a ticket (step 3). This will help expedite the DCV process.

1. Create a CNAME record on your domain's DNS pointing to your regular hostname `clientcode.tt.omtrdc.net`. For example, if your client code is cnamecustomer and your proposed hostname is `target.example.com`, your DNS CNAME record should look something like this:

   ```
   target.example.com  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

1. Open an [Adobe Client Care ticket requesting CNAME support](https://docs.adobe.com/content/help/en/target/using/cmp-resources-and-contact-information.html#reference_ACA3391A00EF467B87930A450050077C) for your [!DNL Target] calls.

   Adobe will work with DigiCert to purchase and deploy your certificate on Adobe's production servers. DigiCert will initiate the DCV process and Adobe Client Care will notify you when your implementation is ready.

1. After completing the preceding tasks and Adobe Client Care has notified you that the implementation is ready, you must update the `serverDomain` to the new CNAME in at.js.

## Frequently Asked Questions

The following information answers frequently asked questions about requesting and implementing CNAM support in [!DNL Target]:

### Can I provide my own certificate? If so, what's the process?

Yes, you can provide your own certificate, to do so:

1. Skip step 1 above, but complete steps 2 and 3. When you open an Adobe Client Care ticket (step 3), let them know you'll be providing your own certificate.

   Adobe will generate and send you a certificate signing request (CSR).

1. Use the CSR to purchase the certificate through your chosen certificate authority (CA).

1. Send the new public certificate to Adobe. Adobe representatives will deploy the public certificate on its production servers.

1. Complete step 4 after Adobe Client Care has notified you that the implementation is ready.

### I already have a CNAME implementation for [!DNL Adobe Analytics], can we use the same certificate or hostname?

No, [!DNL Target] requires a separate hostname and certificate.

### Is my current implementation of Target impacted by ITP 2.1 or 2.2?

In a Safari browser, navigate to your website on which you have a Target JavaScript library. If you see a Target cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.1 or 2.2.

ITP issues can be resolved for Target with just an Analytics CNAME. You'll need a separate Target CNAME only in the case of ad-blocking scenarios where Target is blocked.

For more information about ITP, see [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### How can I validate my CNAME implementation is ready for traffic?

Use the following set of commands (in the MacOs or Linux command-line terminal, using bash and curl 7.49+):

1. First paste this bash function into your terminal:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{17,21,22,26,{28..33}}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Next paste this command (replacing `target.example.com` with your hostname):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   If the implementation is ready, you should see output like below. The important part is that all lines show `CN=target.example.com`, which matches our desired hostname. If any of them show `CN=*.tt.omtrdc.net`, the implementation is **not** ready.

   ```
   $ validateEdgeFpsslSni target.example.com
   mboxedge17.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge21.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge22.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge26.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge28.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge29.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge30.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge31.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge32.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge33.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. Validate your new DNS CNAME with another curl request, which should also show `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >If this command fails but the `validateEdgeFpsslSni` command above succeeds, you might need to wait for your DNS updates to fully propagate.
