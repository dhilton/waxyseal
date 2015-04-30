# waxyseal
Produce certificates, licenses, permits that are cryptographically managed. 

Status: pre-alpha, documenting, exploring - see DEV branch for current code.


### Background


Ever wanted to create your own licenses or issue your permits? Well now you can. WaxySeal implements a license / permit / certificate store over the top of a certificate transparency compliant SSL certificate authority. To that end this django web app implements the certificate transparency audit API (for more info read the RFC http://datatracker.ietf.org/doc/rfc6962/ and have a look at the website http://www.certificate-transparency.org/)

By re(mis)using the metadata fields in a standard X.509 (TLS / SSL certificate) and modeling an 'authority' akin to a certificate authority, you can very quickly generate a concept to enable the production of permits and other official certificates. (The real world example that triggered this project was taxi driver licenses)

For more info check out the docs folder.

### Installation

_Development_

To ensure verifiable, repeatable builds we use peep to pip to absolute hashed versions of code, so that we know that from a security POV, the built webapp is as was intended. See SECURITY.md for more thoughts on securing your installation and how to develope securely for waxyseal.

* Create a new python virtualenv
* cd ./src
* run peep install -r requirements.txt

Todo:

* Implement CT public read only API
* Build permit issuing API
* Design URI scheme for certificates.

