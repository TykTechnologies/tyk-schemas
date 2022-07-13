# tyk-schemas

Repository for all schemas compatible with Tyk objects and files.


JSON, YAML and maybe more schemas for various file types and objects used by Tyk products. 
You can use these schemas in your IDE or favourite editor to get autocompletion or code validation of all your Tyk related work.


**This project is an MVP and still WIP**


## Support Status symbols

| Symbol | Description |
| --------- | --------- |
| ✅ | Fully supported |
| ⚠️ | Untested / Requires Documentation |
| ❌️ | Not currently supported |
| NA | Not available |

## Client to Gateway Authentication

| Type        | JSON      | YAML | Comments |
| ----------- | --------- | ---- | --------- |
| Tyk API definition | ⚠️ | ❌️ | - |
| Tyk API OAS definition | ❌️ | ❌️ | - |
| Tyk API definition in Tyk operator | ❌️ | ❌ | - |
| Tyk key definition | ⚠️ | ❌️ | Also referred as "session object" |
| Tyk policy definition | ❌️ | ❌️ | - |
| Tyk OSS gateway config file | ⚠️ | NA | - |
| Tyk Pro gateway config file | ❌️ | NA | - |
| Tyk hybrid gateway config file | ❌️ | NA | - |
| Tyk pump config file | ❌️ | NA | - |
| Tyk dashboard config file | ❌️ | NA | - |
| Tyk Identity broker config file | ❌️ | NA | - |

# Usage
To write in "Tyk language" and feel it's native to your IDE config the settings in your IDE to use the JSON schemas in this repository

## VSCode

1. Open your VSCode `settings.json` as explained [here](https://code.visualstudio.com/docs/languages/json#_mapping-to-a-schema-in-the-workspace).

2. Add the following lines to your `setting.json`:

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

3. If you want intellisense to work for Tyk's config files you need VSCode to recognice `.conf` extension as json. 
   To achieve that add the following:
```json
    "files.associations": {
        "*.conf": "json"
    }
```

4. `cmd+shift+p` to Reload the window

5. Create files with the name convenstions you used in step #2
   - Tyk API definition - use the format `"apidef.*.json"`, for example `"apidef.httpbin.json"`
   - Tyk key definition - use the format `"apikey.*.json"`, for example `"apikey.httpbin-key.json"`
   - Tyk gateway OSS config file - use the format `"tyk.*.conf"`, for example `"tyk.gateway.conf"`


## Goland

Open the project's preferences (`cmd+,`) and under JSON Schema mapping set the access of Goland to the json schemas and the file formats per the example in this screenshot:
<img width="1180" alt="image" src="https://user-images.githubusercontent.com/3155222/154376405-76aec788-6c52-4b66-8141-c28de0651909.png">



