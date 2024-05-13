```
/                                              # Access the Registry
/model                                         # Access the Registry model definition
/GROUPs                                        # Access a Group Type
/GROUPs/gID                                    # Access a Group
/GROUPs/gID/RESOURCEs                          # Access a Resource Type
/GROUPs/gID/RESOURCEs/rID                      # Default Version of a Resource
/GROUPs/gID/RESOURCEs/rID/versions             # Versions of a Resource
/GROUPs/gID/RESOURCEs/rID/versions/vID         # Access a Version of a Resource

/                                              # Access the Registry
/meta                                          # Access the Registry model definition
/groups/ -> All group types
/groups/<groupTypeId>/ all group instances
/groups/<groupTypeId>/<groupInstanceId> -> particular group instance
/groups/<groupTypeId>/<groupInstanceId>/resourceType/ -> all supported resource types
/groups/<groupTypeId>/<groupInstanceId>/resourceType/<resourceTypeId> -> all supported resource types
/groups/<groupTypeId>/<groupInstanceId>/resourceType/<resourceTypeId>/<resourceId> -> all supported resource types
/groups/<groupTypeId>/<groupInstanceId>/resourceType/<resourceTypeId>/<resourceId>/versions/
/groups/<groupTypeId>/<groupInstanceId>/resourceType/<resourceTypeId>/<resourceId>/versions/<versionId>
/groups/<groupTypeId>/<groupInstanceId>/resourceType/<resourceTypeId>/<resourceId>/versions/<versionId>/formats/
/groups/<groupTypeId>/<groupInstanceId>/resourceType/<resourceTypeId>/<resourceId>/versions/<versionId>/formats/<formatId>
/groups/<groupTypeId>/<groupInstanceId>/resourceType/<resourceTypeId>/<resourceId>/versions/default/formats/default
```

```
/groups/endpoints/e1/resourceType/messages/created/versions/v2.json
/groups/endpoints/e1/resourceType/messages/created/versions/v2/meta
/groups/endpoints/e1/resourceType/messages/created/versions/v2/formats/endpoint-spec
/groups/endpoints/e1/resourceType/messages/created/versions/default/formats/default

/.well-known/xregistry.json
  -> which groups are there
  -> points to metamodel
/.well-known/xregistry.model.json

GET /groups/                - JSON Object, which lists all groups
GET /groups/index.json      - Alterantively, if web-server doesn't support / index pages

/groups/schemaGroups/S3/resourceType/
/groups/schemaGroups/S3/resourceType/schemas/BucketCreated/versions/v1/formats/json-schema
/groups/schemaGroups/S3/resourceType/schemas/BucketCreated/versions/v1/formats/json-schema/BucketCreated.json
```

```http
GET /groups/schemaGroups/S3/resourceType/schemas/BucketCreated/versions

{
    "default": "./v1",
    "v1": "./v1"
}
```


```http
GET /model
GET /export
GET /groups/schemaGroups/S3/resourceType/schemas/BucketCreated/versions/v1

{
    "formats": {
        "json-schema": "./formats/json-schema",
        "avro-schema": "./formats/avro-schema"
    }
}
```

```http
GET /model
GET /export
GET /groups/schemaGroups/S3/resourceType/schemas/BucketCreated/versions/v1/formats/json-schema

{
    $schema: "..."
}
```

```
GET /schemaGroups
GET /schemaGroups/S3/schemas/BucketCreated
```

```
/GROUPs                                        # Access a Group Type
/GROUPs/gID                                    # Access a Group
/GROUPs/gID/RESOURCEs                          # Access a Resource Type
/GROUPs/gID/RESOURCEs/rID                      # Default Version of a Resource
/GROUPs/gID/RESOURCEs/rID/versions             # Versions of a Resource
/GROUPs/gID/RESOURCEs/rID/versions/vID         # Access a Version of a Resource
```
