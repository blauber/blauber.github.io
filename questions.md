# Create a Data Vault Project With biGenius

## Settings

### General Settings
The Data Vault implementation is enabled by the following configuration steps.
* Default template settings for Layer “DWH/Core”, Type “Entity”
  * Group “DW_EN_DV_SQL”: Visible=True, Default=True
  * Group “DW_EN_SQL”: Visible=False, Default=False
* Default template settings for Layer “DWH/Core”, Type “Fact”
  * Group “DW_MG_DV_SQL”: Visible=True, Default=True
  * Group “DW_MG_SQL”: Visible=False, Default=False

<img src="/images/DefaultTemplateSettingsForDV.png" data-canonical-src="/images/DefaultTemplateSettingsForDV.png" width="400" height="400" />

### Configuration of Usage of Hash Keys
The default implementation is based on integer sequence numbers for identities.

Hash keys can be used instead of sequence numbers for the identity columns. The following configuration must be applied to enable this feature before any any DWH object is defined.
*	The custom property “UseHashKey” for the project must be set to “True”
*	Custom property "HashKeyAlgorithm" for the project must be set to a supported algorithm. Default value is 'SHA1' with a size of 20 bytes. See SQL Server documentation of function HASHBYTES. 
Adapt the data type of the identity and foreign key default columns to match the size of the selected algorithm.
*	The data type of the default columns “Identity” and “ForeignKey_Identity” of the DWH object types “Entity” and “Fact” must be set to “BINARY (20)”, before any DWH object is defined.






Here is the page for questions ...

_back to main page_

1. Eins
1. Zwei
 1. Drei
 
 **Bold** and _Italic_ and `Code` text
 
 Das ist unser Code
 
 `is this also code
 or what do you mean?` 
 
 wie man sehen kann.

![GitHub Logo](/images/logo.jpg)
Format: ![Alt Text](url)

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

    function fancyAlert(arg) {
      if(arg) {
        $.facebox({div:'#foo'})
      }
    }
    
As Kanye West said:

> We're living the future so
> the present is our past.
