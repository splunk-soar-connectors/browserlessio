[comment]: # "Auto-generated SOAR connector documentation"
# Browserless chrome

Publisher: Stboch  
Connector Version: 1\.0\.4  
Product Vendor: browerless\.io  
Product Name: chrome  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 5\.0\.0  

This app integrates with Browserless\.io Service and browserless/chrome App to execute various investigative actions

### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a chrome asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**URL** |  required  | string | URL for browserless\.io \(if using hosted service\) https\://chrome\.browserless\.io
**token** |  optional  | password | Token for accessing service \(not required if self hosting\)

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[get pdf](#action-get-pdf) - Download a PDF screenshot of the URL  
[get content](#action-get-content) - Get HTML contents of a webpage  
[get screenshot](#action-get-screenshot) - Download a screenshot of the URL  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'get pdf'
Download a PDF screenshot of the URL

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**url** |  required  | URL of website | string |  `url` 
**headerfooter** |  optional  | Display header and footer | boolean | 
**printbackground** |  optional  | Display background images in PDF | boolean | 
**landscape** |  optional  | Print as landscape | boolean | 
**followrefresh** |  optional  | Wait for URL redirects | boolean | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.url | string |  `url` 
action\_result\.parameter\.headerfooter | boolean | 
action\_result\.parameter\.printbackground | boolean | 
action\_result\.parameter\.landscape | boolean | 
action\_result\.parameter\.followrefresh | boolean | 
action\_result\.data | string | 
action\_result\.status | string | 
action\_result\.message | string | 
action\_result\.summary | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'get content'
Get HTML contents of a webpage

Type: **investigate**  
Read only: **True**

Download the HTML code for the URL provided\.

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**url** |  required  | URL of website | string |  `url` 
**followrefresh** |  optional  | Wait for URL redirects | boolean | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.url | string |  `url` 
action\_result\.parameter\.followrefresh | boolean | 
action\_result\.data | string | 
action\_result\.status | string | 
action\_result\.message | string | 
action\_result\.summary | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'get screenshot'
Download a screenshot of the URL

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**url** |  required  | URL of website | string |  `url` 
**type** |  required  | Type of screenshot PNG or JPEG | string | 
**quality** |  required  | Quality of image | numeric | 
**fullpage** |  optional  | Full page screenshot | boolean | 
**followrefresh** |  optional  | Wait for URL redirects | boolean | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.url | string |  `url` 
action\_result\.parameter\.type | string | 
action\_result\.parameter\.quality | numeric | 
action\_result\.parameter\.fullpage | boolean | 
action\_result\.parameter\.followrefresh | boolean | 
action\_result\.data | string | 
action\_result\.status | string | 
action\_result\.message | string | 
action\_result\.summary | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 