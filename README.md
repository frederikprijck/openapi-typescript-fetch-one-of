# OpenAPI TypeScript-Fetch OneOf

An example file showing incorrectly generated code when using OneOf.

To reproduce, either:

- git clone git@github.com:frederikprijck/openapi-typescript-fetch-one-of.git
- cd openapi-typescript-fetch-one-of
- npm i
- npm run generate
- cat src/generated/models/TestUrl.ts

Or

```sh
docker run --rm -v "${PWD}:/local" openapitools/openapi-generator-cli generate \
    -i https://raw.githubusercontent.com/frederikprijck/openapi-typescript-fetch-one-of/main/api.json \
    -g typescript-fetch \
    -o /local/out/typescript-fetch
```

The generated models/TestUrl.ts file contains code that will not compile.

Reported issue on [OpenAPITools/openapi-generator](https://github.com/OpenAPITools/openapi-generator) : https://github.com/OpenAPITools/openapi-generator/issues/14763
