# LiveStreamsApi

All URIs are relative to *https://ws.api.video*

| Method | Description | HTTP request |
| ------------- | ------------- | ------------- |
| [**create()**](LiveStreamsApi.md#create) | Create live stream | **POST** /live-streams |
| [**get()**](LiveStreamsApi.md#get) | Retrieve live stream | **GET** /live-streams/{liveStreamId} |
| [**update()**](LiveStreamsApi.md#update) | Update a live stream | **PATCH** /live-streams/{liveStreamId} |
| [**delete()**](LiveStreamsApi.md#delete) | Delete a live stream | **DELETE** /live-streams/{liveStreamId} |
| [**list()**](LiveStreamsApi.md#list) | List all live streams | **GET** /live-streams |
| [**uploadThumbnail()**](LiveStreamsApi.md#uploadThumbnail) | Upload a thumbnail | **POST** /live-streams/{liveStreamId}/thumbnail |
| [**deleteThumbnail()**](LiveStreamsApi.md#deleteThumbnail) | Delete a thumbnail | **DELETE** /live-streams/{liveStreamId}/thumbnail |


<a name="create"></a>
## **`create()` - Create live stream**


Creates a livestream object.

### Parameters

| Name | Type | Required | Description |
| ------------- | ------------- | ------------- | ------------- |
 | **liveStreamCreationPayload** | [**LiveStreamCreationPayload**](../model/LiveStreamCreationPayload.md)| **yes**|  |


### Return type

Promise<[**LiveStream**](../model/LiveStream.md)>.




---

<a name="get"></a>
## **`get()` - Retrieve live stream**


Get a livestream by id.

### Parameters

| Name | Type | Required | Description |
| ------------- | ------------- | ------------- | ------------- |
 | **liveStreamId** | **string**| **yes**| The unique ID for the live stream you want to watch. |


### Return type

Promise<[**LiveStream**](../model/LiveStream.md)>.




---

<a name="update"></a>
## **`update()` - Update a live stream**


Updates the livestream object.

### Parameters

| Name | Type | Required | Description |
| ------------- | ------------- | ------------- | ------------- |
 | **liveStreamId** | **string**| **yes**| The unique ID for the live stream that you want to update information for such as player details, or whether you want the recording on or off. |
 | **liveStreamUpdatePayload** | [**LiveStreamUpdatePayload**](../model/LiveStreamUpdatePayload.md)| **yes**|  |


### Return type

Promise<[**LiveStream**](../model/LiveStream.md)>.




---

<a name="delete"></a>
## **`delete()` - Delete a live stream**


If you do not need a live stream any longer, you can send a request to delete it. All you need is the liveStreamId.

### Parameters

| Name | Type | Required | Description |
| ------------- | ------------- | ------------- | ------------- |
 | **liveStreamId** | **string**| **yes**| The unique ID for the live stream that you want to remove. |


### Return type

Promise<[**void**](../model/.md)>.




---

<a name="list"></a>
## **`list()` - List all live streams**


Get the list of livestreams on the workspace.

### Parameters

| Name | Type | Required | Description |
| ------------- | ------------- | ------------- | ------------- |
 | **streamKey** | **string**| no| The unique stream key that allows you to stream videos. |
 | **name** | **string**| no| You can filter live streams by their name or a part of their name. |
 | **sortBy** | **string**| no| Allowed: createdAt, publishedAt, name. createdAt - the time a livestream was created using the specified streamKey. publishedAt - the time a livestream was published using the specified streamKey. name - the name of the livestream. If you choose one of the time based options, the time is presented in ISO-8601 format. |
 | **sortOrder** | **&#39;asc&#39; \| &#39;desc&#39;**| no| Allowed: asc, desc. Ascending for date and time means that earlier values precede later ones. Descending means that later values preced earlier ones. For title, it is 0-9 and A-Z ascending and Z-A, 9-0 descending. |
 | **currentPage** | **number**| no| Choose the number of search results to return per page. Minimum value: 1 |
 | **pageSize** | **number**| no| Results per page. Allowed values 1-100, default is 25. |


### Return type

Promise<[**LiveStreamListResponse**](../model/LiveStreamListResponse.md)>.




---

<a name="uploadThumbnail"></a>
## **`uploadThumbnail()` - Upload a thumbnail**


Upload the thumbnail for the livestream.

### Parameters

| Name | Type | Required | Description |
| ------------- | ------------- | ------------- | ------------- |
 | **liveStreamId** | **string**| **yes**| The unique ID for the live stream you want to upload. |
 | **file** | **string \| Readable \| Buffer**| **yes**| The image to be added as a thumbnail. The mime type should be image/jpeg, image/png or image/webp. The max allowed size is 8 MiB. |


### Return type

Promise<[**LiveStream**](../model/LiveStream.md)>.




---

<a name="deleteThumbnail"></a>
## **`deleteThumbnail()` - Delete a thumbnail**


Send the unique identifier for a live stream to delete its thumbnail.

### Parameters

| Name | Type | Required | Description |
| ------------- | ------------- | ------------- | ------------- |
 | **liveStreamId** | **string**| **yes**| The unique identifier of the live stream whose thumbnail you want to delete. |


### Return type

Promise<[**LiveStream**](../model/LiveStream.md)>.




---
