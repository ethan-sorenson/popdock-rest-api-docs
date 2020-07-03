# Entities

## List All Entities

List all entities(lists) currently setup in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entity</h6>
	</div>
</div>

> To retrieve a list of all entities, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/entity" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/entity"
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
        "EntityId": "77c92142-05e4-45db-bc87-001120461c88",
        "Name": "Purchase credit memo lines",
        "EntityGroupId": "001dae89-8baa-48c9-86ee-516502e49719",
        "Type": 25,
        "ConnectorId": "9c9c5ba6-f65c-4eec-9011-7a349f02d7bf",
        "ItemName": "Purchase credit memo lines",
        "ItemSingular": "Purchase credit memo line"
    }
]
```
## List Entity Fields

List all fields available on a specific entity.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/field</h6>
	</div>
</div>

> To retrieve a list of all defined fields on an entity, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/field" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/field"
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
        "EntityFieldId": "7331f958-f96a-4050-9cac-8157e22c448e",
        "EntityId": "fd5d635d-d0c5-4b57-a685-13d9017214eb",
        "FieldNumber": 142,
        "Name": "RMARACC",
        "Type": 101,
        "DefaultField": false,
        "DisplayName": "Accounts receivable account number",
        "Description": false,
        "DecimalPlaces": 0,
        "TableName": "RM00101",
        "Hidden": false
    }
]
```
## List Entity Default Fields

List the default fields as setup on a specific connector entity.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/default-field</h6>
	</div>
</div>

> To retrieve a list of default fields on an entity, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/default-field" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/default-field"
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
        "EntityFieldId": "96f4e124-556d-4dc2-afe1-5e4d2af61314",
        "EntityId": "fd5d635d-d0c5-4b57-a685-13d9017214eb",
        "FieldNumber": 1,
        "Name": "CUSTNMBR",
        "Type": 1,
        "DisplayName": "Customer number",
        "Description": false,
        "DecimalPlaces": 0,
        "TableName": "RM00101",
        "Hidden": false
    }
]
```
## List Entity Favorites

List all favorites on a connector entity.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/favorite</h6>
	</div>
</div>

> To retrieve a list of all favorites on an entity, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/favorite" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/favorite"
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
        "EntityId": "fd5d635d-d0c5-4b57-a685-13d9017214eb",
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
        "TextRemoveBlanks": false
    }
]
```
## List Entity Restrictions


## List Entity Relationships

List all Relationships(detail) on a connector entity.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/relationship</h6>
	</div>
</div>

> To retrieve a list of Relationships(detail) on an entity, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/relationship" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/relationship"
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
        "EntityId": "fd5d635d-d0c5-4b57-a685-13d9017214eb",
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
        "TextRemoveBlanks": false
    }
]
```
## List Entity Actions

List all actions on a connector entity.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/action</h6>
	</div>
</div>

> To retrieve a list of actions on an entity, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/action" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/action"
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
        "ActionId": "ce21c8ec-fc69-42dd-85c1-0281171bbbfe",
        "Name": "Open item",
        "ConfirmationButton": "OK",
        "CancelButton": "Cancel",
        "EntityId": "62c9dbd6-d457-4924-ab12-7fdc7b0867c0",
        "ConnectorId": "403dc704-baaa-4400-8b80-ac8b3b71ba2f",
        "ActionType": 1000,
        "ActionMethod": 4,
        "Icon": 26
    }
]
```