# Properties
(*properties*)

## Overview

### Available Operations

* [extended_search](#extended_search) - Search for properties

## extended_search

Search for properties

### Example Usage

```python
from zillow_rapidapi_client import ZillowRapidapiClient

with ZillowRapidapiClient() as zrc_client:

    res = zrc_client.properties.extended_search()

    # Handle response
    print(res)

```

### Parameters

| Parameter                                                                                                    | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `location`                                                                                                   | *Optional[str]*                                                                                              | :heavy_minus_sign:                                                                                           | Location details (address, county, neighborhood, or Zip code). Required if polygon or coordinates are empty. |
| `page`                                                                                                       | *Optional[int]*                                                                                              | :heavy_minus_sign:                                                                                           | Page number for paginated results. Max value is 20.                                                          |
| `status_type`                                                                                                | [Optional[models.StatusType]](../../models/statustype.md)                                                    | :heavy_minus_sign:                                                                                           | Property status type.                                                                                        |
| `home_type`                                                                                                  | [Optional[models.HomeType]](../../models/hometype.md)                                                        | :heavy_minus_sign:                                                                                           | Property type. Comma-separated list.                                                                         |
| `sort`                                                                                                       | [Optional[models.Sort]](../../models/sort.md)                                                                | :heavy_minus_sign:                                                                                           | Sorting order.                                                                                               |
| `min_price`                                                                                                  | *Optional[float]*                                                                                            | :heavy_minus_sign:                                                                                           | Minimum price filter.                                                                                        |
| `max_price`                                                                                                  | *Optional[float]*                                                                                            | :heavy_minus_sign:                                                                                           | Maximum price filter.                                                                                        |
| `retries`                                                                                                    | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)                                             | :heavy_minus_sign:                                                                                           | Configuration to override the default retry behavior of the client.                                          |

### Response

**[models.PropertySearchResponse](../../models/propertysearchresponse.md)**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| models.APIError | 4XX, 5XX        | \*/\*           |