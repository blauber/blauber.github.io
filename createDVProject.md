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

Hash keys can be used instead of sequence numbers for the identity columns. __The following configuration must be applied to enable this feature before any any DWH object is defined.__
*	The custom property “UseHashKey” for the project must be set to “True”
*	Custom property "HashKeyAlgorithm" for the project must be set to a supported algorithm. Default value is 'SHA1' with a size of 20 bytes. See SQL Server documentation of function HASHBYTES. 
Adapt the data type of the identity and foreign key default columns to match the size of the selected algorithm.
*	The data type of the default columns “Identity” and “ForeignKey_Identity” of the DWH object types “Entity” and “Fact” must be set to “BINARY (20)”, before any DWH object is defined.

<img src="/images/SettingHash1.png" data-canonical-src="/images/SettingHash1.png" width="600" />

*	Remove the term rule for the default column “Identity” for the DWH parts “DW_EN_Hub_TA_SQL” and “DW_EN_Link_TA_SQL”.

<img src="/images/SettingHash2.png" data-canonical-src="/images/SettingHash2.png" width="600" />

# Configure DWH Layers
Now it is time to define the DWH layers. You can configure which layers you want to have. ![Here](configureDWHLayers.md) it is described how this works.

# Configure Source Objects

# Execute Discovery

# Create Staging Objects
