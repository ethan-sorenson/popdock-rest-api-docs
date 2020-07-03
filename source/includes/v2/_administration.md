# Administration

The administration endpoints provide broad endpoints for retrieving information the can be used later for filtering further requests. 

## List Accounts

List all accounts in which the authenticated user is a member.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/account</h6>
	</div>
</div>

> To retrieve a list of accounts, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/account" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/account"
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
        "AccountId": "e5fdbbcf-ae1d-9874-8072-655d134cd4c7",
        "Name": "EU demo",
        "Status": "InternalUse",
        "Currency": "EUR"
    }
]
```
## List Tags

List all tags setup in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/tag</h6>
	</div>
</div>

> To retrieve a list of tags, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/tag" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/tag"
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
        "TagId": "faa12615-7f5d-4dc1-a675-0253c810efbe",
        "Value": "Customers",
        "UserId": "b22b6ee7-230d-4b8d-8e39-f5ca45409efd"
    }
]
```
## List All Entity Groups

List all entity groups currently setup in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entityGroup</h6>
	</div>
</div>

> To retrieve a list of all entity groups, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/entityGroup" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/entityGroup"
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
        "EntityGroupId": "ca0017fc-a7e5-46a2-81cf-016914b727c1",
        "Name": "Financial",
        "ConnectorId": "2f58ad94-6edf-49ca-b2f8-12ef49a0674e"
    }
]
```
## List All Entity Favorites

List all entity favorites currently setup in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/favorite</h6>
	</div>
</div>

> To retrieve a list of all entity favorites, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/favorite" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/favorite"
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
        "FavoriteId": "d1c085c8-9f16-4146-b6f5-cde2772810a5",
        "Name": "Demo Favorite",
        "UserId": "b22b6ee7-230d-4b8d-8e39-f5ca45409efd",
        "Entity": {
            "EntityId": "fd5d635d-d0c5-4b57-a685-13d9017214eb",
            "Name": "Customers",
            "ItemName": "Customers",
            "ItemSingular": "Customers"
        },
        "Connector": {
            "ConnectorId": "2f58ad94-6edf-49ca-b2f8-12ef49a0674e",
            "Name": "Dynamics GP",
            "Icon": "dynamics-gp"
        },
        "CreatedDate": "2020-07-03T09:33:56.963",
        "MaxRecords": 100,
        "ShowRecordCount": true,
        "ViewType": 0,
        "CategoryFieldId": "e0d04d41-18fa-4c2b-a879-1f39f14a4718",
        "ValueFieldId": "e00ba833-f2de-4da2-8393-4da1792eacc3",
        "MaxCategories": 5,
        "ChartType": 0,
        "SummaryMethod": 5,
        "ChartSort": 0,
        "TextFormat": 1,
        "TextShowHeaders": true,
        "TextRemoveBlanks": false,
        "Links": {
            "Data": "https://api.popdock.com/api/v2/favorite/d1c085c8-9f16-4146-b6f5-cde2772810a5/data"
        }
    }
]
```
## List All Entity Actions

List all entity actions currently setup in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/action</h6>
	</div>
</div>

> To retrieve a list of all entity actions, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/action" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/action"
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
        "ActionId": "99b029eb-c5fa-4ed2-b17c-022a5b97caef",
        "Name": "Open return order",
        "ConfirmationButton": "OK",
        "CancelButton": "Cancel",
        "EntityId": "3bc28181-ed8e-4e7d-856e-f74e5226866d",
        "ConnectorId": "403dc704-baaa-4400-8b80-ac8b3b71ba2f",
        "ActionType": 1000,
        "ActionMethod": 4,
        "Icon": 26
    }
]
```