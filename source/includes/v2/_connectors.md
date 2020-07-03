# Connectors

The connector endpoints can be used to retrieve data about the currently configured connectors in Popdock.

## List Connectors

List all connectors currently setup in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/connector</h6>
	</div>
</div>

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
## List Connector Entities

List all entities(lists) currently setup for a connector in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/connector/{{ConnectorId}}/entity</h6>
	</div>
</div>

> To retrieve a list of all connector entities, use this code:

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
## List Connector Entity Groups

List all entity groups currently setup for a connector in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/connector/{{ConnectorId}}/entityGroup</h6>
	</div>
</div>

> To retrieve a list of connector entity groups, use this code:

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
## List Connector Companies

List all companies currently setup for a connector in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/connector/{{ConnectorId}}/company</h6>
	</div>
</div>

> To retrieve a list of all connector companies, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/connector/{{ConnectorId}}/company" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/connector/{{ConnectorId}}/company"
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
        "CompanyId": "dadd9fe4-1819-42ed-a2e4-d4bf3f36bc40",
        "Name": "Fabrikam, Inc.",
        "ConnectorId": "2f58ad94-6edf-49ca-b2f8-12ef49a0674e",
        "DatabaseName": "GPTWO"
    }
]
```