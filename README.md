<p align="center">
  <img src="https://tanukiapp.xyz/statics/images/logo.png" width=400 />
  <img src="https://www.openapis.org/wp-content/uploads/sites/31/2016/10/OpenAPI_Pantone.png" width="400" />
</p>

# Tanuki OpenAPI Schemas

Tanuki is build with OpenAPI specification in mind, to ensure making it easy to develop and portable. It is made essentially by two services, with their respective APIs: AnimeService and ScheduleService.

Each one provides a subset of data which is served combined throught a gateway.

In this repository you will find the OpenAPI schemas for this APIs, allowing you to generate your own clients to consume this services easy.

Official packages for Node.js are provided at [tanukiapp/tanuki-client](https://github.com/tanukiapp/tanuki-client)

## Generate Anime client

```
npx @openapitools/openapi-generator-cli generate \\
  -i ./openapi/v1/catalog-api.yaml \
  -g typescript-fetch \
  -o ./tanuki/catalog \
--additional-properties=typescriptThreePlus=true
```

## Generate Schedule client

```
npx @openapitools/openapi-generator-cli generate \\
  -i ./openapi/v1/schedule-api.yaml \
  -g typescript-fetch \
  -o ./tanuki/schedule \
--additional-properties=typescriptThreePlus=true
```