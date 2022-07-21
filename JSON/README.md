# JSON Schemas

JSON schemas for all the config files and objects used by Tyk products. 

## Support Status symbols

| Symbol | Description |
| --------- | --------- |
| ✅ | Fully supported |
| ⚠️ | Untested / Requires Documentation |
| ❌️ | Not currently supported |
| NA | Not available |

## Client to Gateway Authentication

| Type        | JSON      | YAML | Comments | Draft |
| ----------- | --------- | ---- | --------- | -------- |
| Tyk API definition | ⚠️ | ❌️ | - | 07 |
| Tyk API OAS definition | ❌️ | ❌️ | - | 07 |
| Tyk API definition in Tyk operator | ❌️ | ❌ | - | 07 |
| Tyk key definition | ⚠️ | ❌️ | Also referred as "session object" | 07 |
| Tyk policy definition | ❌️ | ❌️ | - | 07 |
| Tyk OSS gateway config file | ⚠️ | NA | - | 07 |
| Tyk Pro gateway config file | ❌️ | NA | - | 07 |
| Tyk hybrid gateway config file | ❌️ | NA | - | 07 |
| Tyk pump config file | ❌️ | NA | - | 07 |
| Tyk dashboard config file | ❌️ | NA | - | 07 |
| Tyk Identity broker config file | ❌️ | NA | - | 07 |

# Example for usefull usage
To write in "Tyk language" and feel it's native to your IDE configure the settings in your IDE to use the JSON schemas in this repository

## VSCode

Use Tyk VSCode extension to enable VSCode to enforce Tyk JSON schema on various JSON files:

**VSCode installation**
Install [Tyk extension](https://marketplace.visualstudio.com/items?itemName=TykTechnologiesLimited.tyk-schemas).

For Tyk extension to validate the JSON schemas, make sure to create files with the following name conventions:
   - Tyk API definition - use the format `"apidef.*.json"` or  `"TykDefinition-*.json"`. 
     - Example: `"apidef.httpbin.json"`
   - Tyk OAS API definition - use the format `"oasapidef.*.json"` or`"TykOasApiDef-*.json"`
     - Example `"apidef.httpbin.json"` 
   - Tyk key definition - use the format `"apikey.*.json"`
     - Example `"apikey.httpbin-key.json"`
   - Tyk gateway OSS config file - use the format `"tyk.*.conf"`
     - Example `"tyk.gateway.conf"`



## Goland

Follow [this guide](https://www.jetbrains.com/help/go/json.html#8ae73b55) to enforce the Tyk JSON schema validation.
In the **Schema file or URL** field, specify the **Raw version** URL of one of the Tyk schemas that you want. 
For example, for "Tyk OAS API Definition" add the URL https://raw.githubusercontent.com/TykTechnologies/tyk-schemas/main/JSON/draft-04/schema_apidefoas.json

Example for setting JSON schema for "Tyk OAS API Definition":
<img width="1178" alt="image" src="https://user-images.githubusercontent.com/3155222/180099534-ef58b1f2-dc18-4113-b47d-ed789f63da0a.png">

