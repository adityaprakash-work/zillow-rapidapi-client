<!-- Start SDK Example Usage [usage] -->
```python
# Synchronous Example
from zillow_rapidapi_client import ZillowRapidapiClient

with ZillowRapidapiClient() as zrc_client:

    res = zrc_client.properties.extended_search()

    # Handle response
    print(res)
```

</br>

The same SDK client can also be used to make asychronous requests by importing asyncio.
```python
# Asynchronous Example
import asyncio
from zillow_rapidapi_client import ZillowRapidapiClient

async def main():
    async with ZillowRapidapiClient() as zrc_client:

        res = await zrc_client.properties.extended_search_async()

        # Handle response
        print(res)

asyncio.run(main())
```
<!-- End SDK Example Usage [usage] -->