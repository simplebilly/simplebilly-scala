

# NewVersionRequest

Body for uploading a new version. Bytes must already be stored under `file_name` via the object storage API.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fileName** | **String** | Storage key of the already-uploaded bytes. | 
**fileSize** | **Long** |  |  [optional]
**mimeType** | **String** |  |  [optional]
**originalName** | **String** |  |  [optional]
**sha256Hash** | **String** |  |  [optional]



