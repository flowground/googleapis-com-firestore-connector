# ![LOGO](logo.png) Cloud Firestore **flow**ground Connector

## Description

A generated **flow**ground connector for the Cloud Firestore API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/firestore/v1/swagger.json<br/>
Generated at: 2019-05-23T12:13:23+03:00

## API Description

Accesses the NoSQL document database built for automatic scaling, high performance, and ease of application development.


## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Deletes a long-running operation. This method indicates that the client is<br/>
> no longer interested in the operation result. It does not cancel the<br/>
> operation. If the server doesn't support this method, it returns<br/>
> `google.rpc.Code.UNIMPLEMENTED`.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The name of the operation resource to be deleted.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets information about a location.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Resource name for the location.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates a field configuration. Currently, field updates apply only to<br/>
> single field index configuration. However, calls to<br/>
> FirestoreAdmin.UpdateField should provide a field mask to avoid<br/>
> changing any configuration that the caller isn't aware of. The field mask<br/>
> should be specified as: `{ paths: "index_config" }`.<br/>
> <br/>
> This call returns a google.longrunning.Operation which may be used to<br/>
> track the status of the field update. The metadata for<br/>
> the operation will be the type FieldOperationMetadata.<br/>
> <br/>
> To configure the default field settings for the database, use<br/>
> the special `Field` with resource name:<br/>
> `projects/{project_id}/databases/{database_id}/collectionGroups/__default__/fields/*`.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - A field name of the form
`projects/{project_id}/databases/{database_id}/collectionGroups/{collection_id}/fields/{field_path}`

A field path may be a simple field name, e.g. `address` or a path to fields
within map_value , e.g. `address.city`,
or a special field path. The only valid special field is `*`, which
represents any field.

Field paths may be quoted using ` (backtick). The only character that needs
to be escaped within a quoted field path is the backtick character itself,
escaped using a backslash. Special characters in field paths that
must be quoted include: `*`, `.`,
``` (backtick), `[`, `]`, as well as any ascii symbolic characters.

Examples:
(Note: Comments here are written in markdown syntax, so there is an
 additional layer of backticks to represent a code block)
`\`address.city\`` represents a field named `address.city`, not the map key
`city` in the field `address`.
`\`*\`` represents a field named `*`, not any field.

A special `Field` contains the default indexing settings for all fields.
This field's resource name is:
`projects/{project_id}/databases/{database_id}/collectionGroups/__default__/fields/*`
Indexes defined on this `Field` will be applied to all fields which do not
have their own `Field` index configuration.
* `updateMask` - _optional_ - A mask, relative to the field. If specified, only configuration specified
by this field_mask will be updated in the field.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists information about the supported locations for this service.

*Tags:* `projects`

#### Input Parameters
* `filter` - _optional_ - The standard list filter.
* `name` - _required_ - The resource that owns the locations collection, if applicable.
* `pageSize` - _optional_ - The standard list page size.
* `pageToken` - _optional_ - The standard list page token.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists operations that match the specified filter in the request. If the<br/>
> server doesn't support this method, it returns `UNIMPLEMENTED`.<br/>
> <br/>
> NOTE: the `name` binding allows API services to override the binding<br/>
> to use different resource name schemes, such as `users/*/operations`. To<br/>
> override the binding, API services can add a binding such as<br/>
> `"/v1/{name=users/*}/operations"` to their service configuration.<br/>
> For backwards compatibility, the default name includes the operations<br/>
> collection id, however overriding users must ensure the name binding<br/>
> is the parent resource, without the operations collection id.

*Tags:* `projects`

#### Input Parameters
* `filter` - _optional_ - The standard list filter.
* `name` - _required_ - The name of the operation's parent resource.
* `pageSize` - _optional_ - The standard list page size.
* `pageToken` - _optional_ - The standard list page token.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Starts asynchronous cancellation on a long-running operation.  The server<br/>
> makes a best effort to cancel the operation, but success is not<br/>
> guaranteed.  If the server doesn't support this method, it returns<br/>
> `google.rpc.Code.UNIMPLEMENTED`.  Clients can use<br/>
> Operations.GetOperation or<br/>
> other methods to check whether the cancellation succeeded or whether the<br/>
> operation completed despite cancellation. On successful cancellation,<br/>
> the operation is not deleted; instead, it becomes an operation with<br/>
> an Operation.error value with a google.rpc.Status.code of 1,<br/>
> corresponding to `Code.CANCELLED`.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The name of the operation resource to be cancelled.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Exports a copy of all or a subset of documents from Google Cloud Firestore<br/>
> to another storage system, such as Google Cloud Storage. Recent updates to<br/>
> documents may not be reflected in the export. The export occurs in the<br/>
> background and its progress can be monitored and managed via the<br/>
> Operation resource that is created. The output of an export may only be<br/>
> used once the associated operation is done. If an export operation is<br/>
> cancelled before completion it may leave partial data behind in Google<br/>
> Cloud Storage.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Database to export. Should be of the form:
`projects/{project_id}/databases/{database_id}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Imports documents into Google Cloud Firestore. Existing documents with the<br/>
> same name are overwritten. The import occurs in the background and its<br/>
> progress can be monitored and managed via the Operation resource that is<br/>
> created. If an ImportDocuments operation is cancelled, it is possible<br/>
> that a subset of the data has already been imported to Cloud Firestore.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Database to import into. Should be of the form:
`projects/{project_id}/databases/{database_id}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists the field configuration and metadata for this database.<br/>
> <br/>
> Currently, FirestoreAdmin.ListFields only supports listing fields<br/>
> that have been explicitly overridden. To issue this query, call<br/>
> FirestoreAdmin.ListFields with the filter set to<br/>
> `indexConfig.usesAncestorConfig:false`.

*Tags:* `projects`

#### Input Parameters
* `filter` - _optional_ - The filter to apply to list results. Currently,
FirestoreAdmin.ListFields only supports listing fields
that have been explicitly overridden. To issue this query, call
FirestoreAdmin.ListFields with the filter set to
`indexConfig.usesAncestorConfig:false`.
* `pageSize` - _optional_ - The number of results to return.
* `pageToken` - _optional_ - A page token, returned from a previous call to
FirestoreAdmin.ListFields, that may be used to get the next
page of results.
* `parent` - _required_ - A parent name of the form
`projects/{project_id}/databases/{database_id}/collectionGroups/{collection_id}`
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists composite indexes.

*Tags:* `projects`

#### Input Parameters
* `filter` - _optional_ - The filter to apply to list results.
* `pageSize` - _optional_ - The number of results to return.
* `pageToken` - _optional_ - A page token, returned from a previous call to
FirestoreAdmin.ListIndexes, that may be used to get the next
page of results.
* `parent` - _required_ - A parent name of the form
`projects/{project_id}/databases/{database_id}/collectionGroups/{collection_id}`
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a composite index. This returns a google.longrunning.Operation<br/>
> which may be used to track the status of the creation. The metadata for<br/>
> the operation will be the type IndexOperationMetadata.

*Tags:* `projects`

#### Input Parameters
* `parent` - _required_ - A parent name of the form
`projects/{project_id}/databases/{database_id}/collectionGroups/{collection_id}`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-firestore-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
