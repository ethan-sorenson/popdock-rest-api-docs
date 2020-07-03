# Developer

Retrieve information from the developer section of Popdock.

## List Widgets

List all widgets currently setup in the Popdock instance.

There are currently are 6 types of widget.

Number | Type
--------- | -------
1 | Application
3 | Favorite
5 | Summary
6 | Single record
7 | Sidebar
9 | Cards

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/widget</h6>
	</div>
</div>

> To retrieve a list of widgets, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/widget" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/widget"
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {{token}}'
}

response = requests.request("GET", url, headers=headers)

print(response.text.encode('utf8'))
```
> The above command returns the following json:

```json
[
    {
        "WidgetId": "37e76b3a-e3a9-4b92-1234-1e6bf9e1853c",
        "AccountId": "e5fdbbcf-ae1d-4cb6-1234-655d134cd4c7",
        "Name": "BC Demo Items",
        "Type": 6,
        "ConnectorId": "a453ca61-72ee-487b-123-c3a54424d350",
        "EntityId": "5c66e231-fcaa-4db1-a8f5-c8c3853f2103",
        "Height": 100,
        "Width": 100,
        "HeightType": 2,
        "WidthType": 2,
        "Token": "325fe36a-805a-4a89-4212-a960d525d17b",
        "CompanyId": "b823d076-fa9a-1234-b978-590983e2c754",
        "UserId": "b22b6ee7-230d-4b8d-8e39-f5ca45409efd",
        "Endpoint": "OmvnN6njkkuonx5r-eGFPA"
    }
]
```
## List Widget Parameters

List all widget parameters for a defined widget

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/widget/{{WidgetId}}/parameter</h6>
	</div>
</div>

> To retrieve a list of parameters, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/widget/{{WidgetId}}/parameter" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/widget/{{WidgetId}}/parameter"
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {{token}}'
}

response = requests.request("GET", url, headers=headers)

print(response.text.encode('utf8'))
```
> The above command returns the following json:

```json
[
    {
        "WidgetParameterId": "ceff8252-3af1-4de6-a1dc-8497bc76ab49",
        "WidgetId": "37e76b3a-e3a9-4b92-1234-1e6bf9e1853c",
        "Name": "no",
        "FieldId": "9aadcb63-3fca-487a-bcab-4e4975385a8f",
        "Required": false
    }
]
```
## List API Endpoints

List all API endpoints defined in Popdock.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/endpoint</h6>
	</div>
</div>

> To retrieve a list of API endpoints, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/endpoint" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/endpoint"
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {{token}}'
}

response = requests.request("GET", url, headers=headers)

print(response.text.encode('utf8'))
```
> The above command returns the following json:

```json
[
    {
        "EndpointId": "31434eeb-79b3-48a2-86a0-2c689198a199",
        "Endpoint": "Demo"
    }
]
```
## List API Endpoint Parameters

List parameters for an API endpoint defined in Popdock.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/endpoint/{{EndpointId}}/parameters</h6>
	</div>
</div>

> To retrieve a list of parameters, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/endpoint/{{EndpointId}}/parameters" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/endpoint/{{EndpointId}}/parameters"
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {{token}}'
}

response = requests.request("GET", url, headers=headers)

print(response.text.encode('utf8'))
```
> The above command returns the following json:

```json
{
    "EndpointId": "da488562-8800-4720-b88e-709edd2efd4d",
    "Endpoint": "ERP Data",
    "Entity": {
        "EntityId": "4c1a8b08-01f1-43af-987e-1384e4f279bc",
        "Name": "Merge Sales Invoices",
        "ItemName": "Merge Sales Invoices",
        "ItemSingular": "Merge Sales Invoice"
    },
    "Company": {
        "CompanyId": "a477ff7d-f9eb-4f3d-bc64-8d834f03ab93",
        "Name": "CRONUS US"
    }
}
```