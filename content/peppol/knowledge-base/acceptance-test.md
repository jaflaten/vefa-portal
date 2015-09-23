+++

title = "Acceptance test"
group = "Governance"
type = "article"

+++

Testing is performed to ensure introduction of a new provider in the network does not cause instability and problems.

## Prerequisites

The following steps must be done in the [Governance model](/peppol/knowledge-base/governance-model/):

1. Apply for OpenPEPPOL Membership.
1. Sign and send Transport Infrastructure Agreement (TIA) to PEPPOL Authority.

Provider subject to testing will receive enrollment information to generate certificate in the OpenPEPPOL TEST PKI chain.

Generated certificate must be installed in the access point of choice.

**Tips:** Make sure to do self-testing before initiating acceptance test. Provider is free to use the [Access point (test)](/peppol/tools/ap-test/) provided by Difi to perform self-testing.

## Configuration

Providers using [Oxalis](/peppol/tools/oxalis/) must update oxalis-global.properties to contain this values:

```
oxalis.pki.version=V2
oxalis.operation.mode=TEST
oxalis.sml.hostname=acc.edelivery.tech.ec.europa.eu
```

Other products must be configured accordingly.

## Performing acceptance test

### Inform Difi

Before testing starts, make sure to inform Difi by sending mail to [ap@difi.no](mailto:ap@difi.no) containing this information:

* Who performs the test
* Contact information
* URL of access point
* File containing certificate **(Do not send private key!)**

### Send document to Difi

Send a document of choice to [9908:810418052](https://test-vefa.difi.no/smp/9908/810418052). Find your document in [Inbound files](/peppol/tools/ap-test/) and send the URL to [ap@difi.no](mailto:ap@difi.no) for verification of sending.

### Receive document to Difi

Difi will send a document of choice to access point. Provider will receive a mail with question regarding the content to confirm successful sending.

## Send test report

Provider subject to testing must use results from testing to complete a [test report](/docs/peppol/aptest.xlsx) and send it to [ap@difi.no](mailto:ap@difi.no) (do not reply to earlier mail) within one week from completing testing.

Upon accepted test report by Difi will enrollment to generate certificate in the OpenPEPPOL PRODUCTION PKI chain become available to provider.