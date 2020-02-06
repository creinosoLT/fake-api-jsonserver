# USAGE OF THE FAKE API
This *fake api* works with the [JsonServer](https://www.npmjs.com/package/json-server) library from [NPM](https://www.npmjs.com/), you can use whatever method you wold normally use to make all basic HTTP requests to this API, so you're free to call it however you like.

## MAKING A POST
In order to make a POST request to the API you must edit first the `db.json` file, every item of the JSON is considered as a *Father* of the objects under itself, so every one of these *Fathers* will work as a specific endpoint.

E.g:
```
{
    "shipments": [{}, {}],
    "quotes": [{}, {}],
    "reports": [{}, {}]
}

```
In the example above the *shipments*, *quotes* and *reports* are cosidered as **Fathers** so every single object will be inside of these **Fathers**

E.g

```
{
    "shipments": [
    {
        "id": "001",
        "cDate": "Jan 09 2020",
        "owner": "Graphic INC",
        "pReference": "REF001",
        "pDeliver": "Jan 07 2020",
        "carrier": "SAIA LTL FREIGHT",
        "oDestiny": "Germany/USA",
        "status": "Delivered"
    },
    ....... more shipments
    ]

```
In the example above in order to make a `GET` request fot the *001 ID shipment*, you do it as you normally do with any other request.

So if you are doing a `POST` request be sure to have defined your object shape in the first place.