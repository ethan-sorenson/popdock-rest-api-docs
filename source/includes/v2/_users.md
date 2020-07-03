# Users

## List All Users

List all users currently setup in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/user</h6>
	</div>
</div>

> To retrieve a list of all users, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/user" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/user"
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
        "UserId": "b22b6ee7-230d-4b8d-8e39-f5ca45409efd",
        "FirstName": "EU",
        "LastName": "demo",
        "Email": "eu.demo@eonesolutions.com",
        "Status": "Active",
        "Created": "2019-08-05T11:04:11",
        "Modified": "2020-07-02T14:42:58.55",
        "EmailVerified": true,
        "Name": "EU demo",
        "DisplayName": "EU demo",
        "DisplayEmail": "eu.demo@eonesolutions.com"
    }
]
```
## List All Teams

List all teams currently setup in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/team</h6>
	</div>
</div>

> To retrieve a list of all teams, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/team" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/team"
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
        "TeamId": "87592bc6-f970-4517-bbf3-1b47a1c3aa35",
        "AccountId": "e5fdbbcf-ae1d-4cb6-8072-655d134cd4c7",
        "Name": "Admin",
        "Description": "Administration"
    }
]
```
## List All Team Members

List all team members currently setup in the Popdock instance.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/team/{{TeamId}}/member</h6>
	</div>
</div>

> To retrieve a list of all team members, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/team/{{TeamId}}/member" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/team/{{TeamId}}/member"
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
        "TeamMemberId": "18916060-a98f-4691-a996-d88a572cdc8c",
        "TeamId": "87592bc6-f970-4517-bbf3-1b47a1c3aa35",
        "UserId": "b22b6ee7-230d-4b8d-8e39-f5ca45409efd"
    }
]
```