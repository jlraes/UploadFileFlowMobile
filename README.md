# SFDX  App

## Dev, Build and Test
SCRATCH ORG
sfdx force:org:create -s -f config/project-scratch-def.json -a "UploadFileFlowMobile"
sfdx force:source:push

CLASSIC ORG
sfdx force:source:convert -d mdapioutput/

sfdx force:mdapi:deploy -d ./mdapioutput -u YourOrgAlias -w 100


## Resources
https://developer.salesforce.com/docs/atlas.en-us.salesforce_vpm_guide.meta/salesforce_vpm_guide/vpm_files.htm
https://releasenotes.docs.salesforce.com/en-us/spring18/release-notes/rn_forcecom_flow_file.htm
https://salesforcesidekick.com/2018/01/15/the-lowdown-on-uploading-a-file-inside-a-flow/


## Description of Files and Directories
Process Automation Settings > Enable Lightning runtime for flows

Add existing action to pagelayouts
or 
create new action on other objects, referencing the FlowUploadFile flow.
The recordId variable is automatically linked with the Record Id
When added as an action, the button will be visible on the Salesforce app also.

The flow can also be added to a lightning page (this will not be visible for mobile devices).
## Issues


