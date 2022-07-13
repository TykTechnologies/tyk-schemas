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

## VSCode example

1. VSCode installation - Install [Tyk extension](https://marketplace.visualstudio.com/items?itemName=TykTechnologiesLimited.tyk-schemas).
Or
2. Manual instalation - 
3. Open your VSCode `settings.json` as explained [here](https://code.visualstudio.com/docs/languages/json#_mapping-to-a-schema-in-the-workspace).
   Add the following lines to your `setting.json`:

```json
"json.schemas": [
          {
            "fileMatch": [
                "tyk.*.conf"
            ],
            "url": "https://raw.githubusercontent.com/letzya/tyk-schemas/main/schema_tyk.oss.conf"
        },
        {
            "fileMatch": [
                "apikey.*.json"
            ],
            "url": "https://raw.githubusercontent.com/letzya/tyk-schemas/main/schema_apikey.json"
        },
        {
            "fileMatch": [
                "apidef.*.json"
            ],
            "url": "https://raw.githubusercontent.com/letzya/tyk-schemas/main/schema_apidef_lean.json"
        },
    ],
```

To get intellisense to work for Tyk's config files you need VSCode to recognice `.conf` extension as json. 
   To achieve that add the following:
```json
    "files.associations": {
        "*.conf": "json"
    }
```

`cmd+shift+p` to Reload the window

Create files with the name convenstions you used in step #2
   - Tyk API definition - use the format `"apidef.*.json"`, for example `"apidef.httpbin.json"`
   - Tyk key definition - use the format `"apikey.*.json"`, for example `"apikey.httpbin-key.json"`
   - Tyk gateway OSS config file - use the format `"tyk.*.conf"`, for example `"tyk.gateway.conf"`


## Goland

Open the project's preferences (`cmd+,`) and under JSON Schema mapping set the access of Goland to the json schemas and the file formats per the example in this screenshot:
<img width="1180" alt="image" src="https://user-images.githubusercontent.com/3155222/154376405-76aec788-6c52-4b66-8141-c28de0651909.png">



