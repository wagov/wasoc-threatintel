# WASOC Threat Intelligence Repository


This repository contains Threat Intelligence content from Western Australian Security Operations Center.

## Table of Contents

1) [Analytic Rules and deployments](#analytic-rules-for-detections-with-threat-intelligence)
2) [Analytic Rule deployment guide](#analytic-rule-deployment-guide)


<br>
<!-- Empty line for styling -->
</br>

<br>
<!-- Empty line for styling -->
</br>

<div align="center">

## Analytic Rules for detections with Threat Intelligence

</div>

The following Analytic rules can be deployed to Microsoft Sentinel environment to enable the detection of suspicious/potentially malicious activity based on Threat Intelligence shared by WASOC.

| Rule Name | Deploy Rule |
|-|-|
| Phishing domain-name accessed by users - DeviceNetworkEvents | [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fwagov%2Fwasoc-threatintel%2Frefs%2Fheads%2Fmain%2Fanalytic-rules%2FWASOC-Intelligence-a-known-phishing-domain-name-has-been-accessed-by-user-DeviceNetworkEvents.json) |
| Phishing Url accessed by users - DeviceEvents | [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fwagov%2Fwasoc-threatintel%2Frefs%2Fheads%2Fmain%2Fanalytic-rules%2FWASOC-Intelligence-a-known-phishing-url-has-been-accessed-by-a-user-DeviceEvents.json) |
| Phishing Url clicked by users - UrlClickEvents | [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fwagov%2Fwasoc-threatintel%2Frefs%2Fheads%2Fmain%2Fanalytic-rules%2FWASOC-Intelligence-a-known-phishing-URL-has-been-clicked-by-user-UrlClickEvents.json) |
| Suspicious sign-in attempts from malicious IPs related to phishing - OfficeActivity | [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fwagov%2Fwasoc-threatintel%2Frefs%2Fheads%2Fmain%2Fanalytic-rules%2FWASOC-Intelligence-a-suspicious-sign-ins-attempts-from-known-malicious-IP-address-related-to-phishing-campaign.json) |
| Office Activity from malicious IPs related to phishing - OfficeActivity | [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fwagov%2Fwasoc-threatintel%2Frefs%2Fheads%2Fmain%2Fanalytic-rules%2FWASOC-Intelligence-Observed-OfficeActivity-from-known-malicious-IP-address-related-to-phishing.json) |
| Phishing email potentially delivered to users mailbox | [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fwagov%2Fwasoc-threatintel%2Frefs%2Fheads%2Fmain%2Fanalytic-rules%2FWASOC-Intelligence-Phishing-email-potentially-delivered-to-user-mailbox.json) |
| Detect inbound traffic from IP address(s) known (by WASOC) for active exploitation of vulnerabilities| [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fwagov%2Fwasoc-threatintel%2Frefs%2Fheads%2Fmain%2Fanalytic-rules%2FWASOC-Intelligence-Successful-inbound-traffic-to-AzureDiagnostics-from-ip-address-monitored-by-WA-SOC-known-to-actively-exploit-new-vulnerabilities.json) |

<br>
<!-- Empty line for styling -->
</br>

### Analytic Rule Deployment guide
---
Click on the Deploy to Azure button on the table in '[Analytic Rules and deployments](#analytic-rules-for-detections-with-threat-intelligence)' and follow the below instructions for the deployment.

<br>
<!-- Empty line for styling -->
</br>

#### Step 1

Fill in the relevant details of the listed items as noted below.

![page1](/media/Custom-Deployment-image1-steps.jpeg)

1. Select the **Subscription** your workspace is under
2. Select the specific **Resource Group**
3. Select the **Region**
4. Provide your **Workspace Name** found under Log Analytics workspace settings
5. Leave the newGuid() to generate a unique Rule Id for your rule

<br>
<!-- Empty line for styling -->
</br>

#### Step 2

Ensure the details provided in the previous stage are all accurate and proceed to the next step.

![page2](/media/Custom-Deployment-image2-steps.jpeg)

<br>
<!-- Empty line for styling -->
</br>

#### Step 3

If the analytic rule has been successfully deployed, you will see the below screen. Click on the '**Go to Resource**' button to view the deployed analytic rule(s). You can also navigate to the ***Analytics*** blade in the Microsoft Sentinel environment to confirm if the rules have successfully been deployed.

![page3](/media/Custom-Deployment-image3-step.jpeg)


