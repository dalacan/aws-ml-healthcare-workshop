# AWS ML Healthcare Workshop

## Introduction

## Lab Instruction

[Workshop Link Placeholder]

## Deploy your Working Environment

The first step is to deploy a Cloudformation template that will perform most of the initial setup for you.

1. Download the cloudformation template

Go to the following URL https://raw.githubusercontent.com/dalacan/aws-ml-healthcare-workshop/blob/master/aws-ml-healthcare-worshop.yaml, right click 'Save As' and download the cloudformation template.

**Note** Make sure you save the file as a .yaml file.

2. Create a new cloud formationstack

In another browser window or tab, login to your AWS account. Once you have done that, open the link below in a new tab to start the process of deploying the items you need via CloudFormation.

[![Launch Stack](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png)](https://console.aws.amazon.com/cloudformation/home#/stacks/new?stackName=HealthcareWorkshop)

3. Upload the cloud formation template

Select `Upload a template`,  click `Choose file` and select the cloudformation template file you've just downloaded and then click `Next`.

![CloudformationWizard1](static/images/step3.png)

4. Specify stack details

In this section, **optionally** specify the following options:
    
        1. Stack Name - Change the stack name to something more relevant if required.
        2. Notebook Name - Change the name of your SageMaker notebook which you will be using if required.
        3. Volumen Size - Set the size of SageMaker EBS volume (default is 10GB). If you expect to load a larger dataset (i.e. if you want to reuse this lab to experiment with larger dataset), increase this accordingly.

When you're done, click the `Next` button at the bottom of the page
![CloudformationWizard2](static/images/step4.png)

5. Configure stack options

All of the defaults in this section will be sufficient to complete the lab. If you have any custom requirements, please alter as required. Once you're done, click the `Next` button to continue.

Finally, in the next section, scroll to the bottom of the page and check the checkbox to enable the template to create IAM resources and click the `Create stack` button.

![CloudformationWizard3](static/images/step5a.png)

It will take a few minutes to provision the resources required for the lab. Once it is completed, navigate to the `SageMaker` service by clicking `Services` in tht top of the console and then search for `SageMaker` and click on the service.

![SageMaker](static/images/step5b.png)

6. Launch the SageMaker notebook

Click on Notebook instance and open the `aws-ml-healthcare-workshop` notebook (or the name of the notebook you provided in Cloudformation) by clicking `Open JupyterLab`

![SageMaker](static/images/step6.png)


## Cleanup
Once you're done with the lab, please make sure you follow the instructions at the end of the notebook to delete all the resources you created in your AWS account. Once you have done that, go to the **CloudFormation** service in the AWS console and delete the `HealthcareWorkshop` stack.

---

## References