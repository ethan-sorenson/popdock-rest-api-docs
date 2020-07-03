# Connectors

The connector endpoints can be used to retrieve data about the currently configured connectors in Popdock.

## List Connectors

> To retrieve a list of connectors, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/connector" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/connector"
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
        "ConnectorId": "2f58ad94-6edf-49ca-b2f8-12ef49a06700",
        "ConnectorType": 13,
        "Name": "Dynamics GP",
        "CompanyPrompt": "Company",
        "CompanyPluralPrompt": "Companies",
        "Icon": "dynamics-gp",
        "CreatedDate": "2020-06-18T14:28:57.687",
        "NumberOfCompanies": 3,
        "NumberOfGroups": 11,
        "Links": {
            "Entities": "https://api.popdock.com/api/v2/connector/2f58ad94-6edf-49ca-b2f8-12ef49a06700/entity",
            "Entity groups": "https://api.popdock.com/api/v2/connector/2f58ad94-6edf-49ca-b2f8-12ef49a06700/entity-group",
            "Companies": "https://api.popdock.com/api/v2/connector/2f58ad94-6edf-49ca-b2f8-12ef49a06700/company"
        }
    }
]
```
List all connectors currently setup in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/connector</h6>
	</div>
</div>


## List All Entities

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
List all entities(lists) currently setup in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entity</h6>
	</div>
</div>

## List Connector Entities

> To retrieve a list of all entities, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/connector/{{ConnectorId}}/entity" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/connector/{{ConnectorId}}/entity"
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
        "EntityId": "b69f8a64-e996-4bdb-ab04-f49630778fa1",
        "Name": "Account summary",
        "EntityGroupId": "ca0017fc-a7e5-46a2-81cf-016914b727c1",
        "Type": 13,
        "ConnectorId": "2f58ad94-6edf-49ca-b2f8-12ef49a0674e",
        "ItemName": "Account summary",
        "ItemSingular": "Account summary",
        "NumberOfFavorites": 0,
        "Links": {
            "Fields": "https://api.popdock.com/api/v2/entity/b69f8a64-e996-4bdb-ab04-f49630778fa1/field",
            "Default fields": "https://api.popdock.com/api/v2/entity/b69f8a64-e996-4bdb-ab04-f49630778fa1/default-field",
            "Favorites": "https://api.popdock.com/api/v2/entity/b69f8a64-e996-4bdb-ab04-f49630778fa1/favorite",
            "Data": "https://api.popdock.com/api/v2/entity/b69f8a64-e996-4bdb-ab04-f49630778fa1/data"
        }
    }
]
```
List all entities(lists) currently setup for a connector in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/connector/{{ConnectorId}}/entity</h6>
	</div>
</div>

## List All Entity Groups

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
List all entity groups currently setup in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entityGroup</h6>
	</div>
</div>

## List Connector Entity Groups

> To retrieve a list of all entity groups, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/connector/{{ConnectorId}}/entityGroup" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/connector/{{ConnectorId}}/entityGroup"
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
List all entity groups currently setup for a connector in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/connector/{{ConnectorId}}/entityGroup</h6>
	</div>
</div>

## List Entity Fields

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
List all fields available on a specific entity.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/field</h6>
	</div>
</div>

## List Entity Default Fields

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
List the default fields as setup on a specific connector entity.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/default-field</h6>
	</div>
</div>

## List Entity Favorites

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
List all favorites on a connector entity.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/favorite</h6>
	</div>
</div>

## List Entity Restrictions


## List Entity Relationships

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
List all Relationships(detail) on a connector entity.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/relationship</h6>
	</div>
</div>

## List Connector Entity Groups


## List Connector Companies

## List All Actions