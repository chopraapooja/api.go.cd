## Get one agent

```shell
$ curl 'https://ci.example.com/go/api/agents/adb9540a-b954-4571-9d9b-2f330739d4da' \
      -u 'username:password' \
      -H 'Accept: application/vnd.go.cd.v1+json'
```

> The above command returns JSON structured like this:

```http
HTTP/1.1 200 OK
Content-Type: application/vnd.go.cd.v1+json; charset=utf-8
```

```json
{
  "_links": {
    "self": {
      "href": "https://ci.example.com/go/api/agents/adb9540a-b954-4571-9d9b-2f330739d4da"
    },
    "doc": {
      "href": "http://api.go.cd/#agents"
    },
    "find": {
      "href": "https://ci.example.com/go/api/agents/:uuid"
    }
  },
  "uuid": "adb9540a-b954-4571-9d9b-2f330739d4da",
  "hostname": "ketanpkr.corporate.thoughtworks.com",
  "ip_address": "10.12.20.47",
  "enabled": true,
  "sandbox": "/Users/ketanpadegaonkar/projects/gocd/gocd/agent",
  "status": "Idle",
  "operating_system": "Mac OS X",
  "free_space": 85890146304,
  "resources": ["java", "linux", "firefox"],
  "environments": ["perf", "UAT"]
}
```

Gets an agent by its unique identifier (uuid)

### HTTP Request

`GET /go/api/agents/:uuid`

### Returns

An [agent object](#the-agent-object).
