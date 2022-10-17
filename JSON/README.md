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

| Schema Description        | JSON      | YAML | Comments | Draft | When is it used
| ----------- | --------- | ---- | --------- | -------- | -------- |
| Tyk Gateway API definition | ⚠️ | ❌️ | - | 07 | An OpenAPI Spec object |
| Tyk dashboard API definition | ⚠️ | ❌️ | - | 07 | An OpenAPI Spec object |
| Tyk API OAS definition | ❌️ | ❌️ | - | 07 | An OpenAPI Spec object |
| Tyk dashboard API OAS definition | ⚠️ | ❌️ | - | 07 | An OpenAPI Spec object |
| Tyk API definition in Tyk operator | ❌️ | ❌ | - | 07 | Tyk operator object |
| Tyk Gateway key definition | ⚠️ | ❌️ | Also referred as "session object" | 07 | An OpenAPI Spec object |
| Tyk dashboard key definition | ⚠️ | ❌️ | Also referred as "session object" | 07 | An OpenAPI Spec object |
| Tyk Gateway policy definition | ❌️ | ❌️ | - | 07 | An OpenAPI Spec object |
| Tyk dashboard policy definition | ❌️ | ❌️ | - | 07 | An OpenAPI Spec object |
| Tyk OSS gateway config file | ⚠️ | NA | Examples and default values specific to gateway in an open source deployment | 07 | Config file |
| Tyk Self-managed gateway config file | ❌️ | NA | Examples and default values specific to gateway in a self managed deployment | 07 | Config file |
| Tyk hybrid gateway config file | ❌️ | NA | Examples and default values specific to gateway in a hybrid deployment | 07 | Config file |
| Tyk pump config file | ❌️ | NA | - | 07 | Config file |
| Tyk dashboard config file | ❌️ | NA | - | 07 | Config file |
| Tyk Identity broker config file | ❌️ | NA | - | 07 | Config file |
| Tyk Self-managed user | ❌️ | NA | - | 07 | An OpenAPI Spec object |
| Tyk Self-managed user group | ❌️ | NA | - | 07 | An OpenAPI Spec object |

# Example for usefull usage

1. Write correct and valid API calls.
2. Write code that etend Tyk and make sure the input objects are correct.
3. You can connect your IDE to these JSON schemas to be able to validate and do semi linting to the config files.
4. Connecting to the IDE also gives you auto-completeion capabilities along with default values, examples and helpful field descriptions.
5. ...fill free to use it to innovate

### VS Code IDE

Tyk VS Code extention is an existing project that is already using this repo. For more details check [Tyk extension](https://marketplace.visualstudio.com/items?itemName=TykTechnologiesLimited.tyk-schemas) or our blog [Get productive with the Tyk IntelliSense extension](https://tyk.io/blog/get-productive-with-the-tyk-intellisense-extension/)


### Goland IDE

Follow [Jetbrains guide](https://www.jetbrains.com/help/go/json.html#8ae73b55) to enforce the Tyk JSON schema validation.
In the **Schema file or URL** field, specify the **Raw version** URL of one of the Tyk schemas that you want. 
For example, for "Tyk OAS API Definition" add the URL https://raw.githubusercontent.com/TykTechnologies/tyk-schemas/main/JSON/draft-04/schema_apidefoas.json

Example for setting JSON schema for "Tyk OAS API Definition":
<img width="1178" alt="image" src="https://user-images.githubusercontent.com/3155222/180099534-ef58b1f2-dc18-4113-b47d-ed789f63da0a.png">

