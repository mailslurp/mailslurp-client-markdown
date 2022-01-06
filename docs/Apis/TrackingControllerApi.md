# TrackingControllerApi

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createTrackingPixel**](TrackingControllerApi#createTrackingPixel) | **POST** /tracking/pixels | Create tracking pixel
[**getAllTrackingPixels**](TrackingControllerApi#getAllTrackingPixels) | **GET** /tracking/pixels | Get tracking pixels
[**getTrackingPixel**](TrackingControllerApi#getTrackingPixel) | **GET** /tracking/pixels/{id} | Get pixel


<a name="createTrackingPixel"></a>
# **createTrackingPixel**
> TrackingPixelDto createTrackingPixel(CreateTrackingPixelOptions)

Create tracking pixel

    Create a tracking pixel. A tracking pixel is an image that can be embedded in an email. When the email is viewed and the image is seen MailSlurp will mark the pixel as seen. Use tracking pixels to monitor email open events. You can receive open notifications via webhook or by fetching the pixel.

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateTrackingPixelOptions** | [**CreateTrackingPixelOptions**](../Models/CreateTrackingPixelOptions)|  |

### Return type

[**TrackingPixelDto**](../Models/TrackingPixelDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

<a name="getAllTrackingPixels"></a>
# **getAllTrackingPixels**
> PageTrackingPixelProjection getAllTrackingPixels(page, size, sort, searchFilter, since, before)

Get tracking pixels

    List tracking pixels in paginated form

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Integer**| Optional page index in list pagination | [optional] [default to 0]
 **size** | **Integer**| Optional page size in list pagination | [optional] [default to 20]
 **sort** | **String**| Optional createdAt sort direction ASC or DESC | [optional] [default to ASC] [enum: ASC, DESC]
 **searchFilter** | **String**| Optional search filter | [optional] [default to null]
 **since** | **Date**| Filter by created at after the given timestamp | [optional] [default to null]
 **before** | **Date**| Filter by created at before the given timestamp | [optional] [default to null]

### Return type

[**PageTrackingPixelProjection**](../Models/PageTrackingPixelProjection)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

<a name="getTrackingPixel"></a>
# **getTrackingPixel**
> TrackingPixelDto getTrackingPixel(id)

Get pixel

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**UUID**](../Models/)|  | [default to null]

### Return type

[**TrackingPixelDto**](../Models/TrackingPixelDto)

### Authorization

[API_KEY](../README#API_KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

