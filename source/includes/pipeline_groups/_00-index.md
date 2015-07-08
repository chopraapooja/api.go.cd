## Config listing

```shell
$ curl 'https://ci.example.com/go/api/config/pipeline_groups' \
      -u 'username:password'
```

> The above command returns JSON structured like this:

```http
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
```

```json
[
  {
    "pipelines": [
      {
        "stages": [
          {
            "name": "up42_stage"
          }
        ],
        "name": "up42",
        "materials": [
          {
            "description": "URL: https://github.com/gocd/gocd, Branch: master",
            "fingerprint": "2d05446cd52a998fe3afd840fc2c46b7c7e421051f0209c7f619c95bedc28b88",
            "type": "Git"
          }
        ],
        "label": "${COUNT}"
      }
    ],
    "name": "first"
  }
]
```

This API is built primarily to support rendering of value stream mapping. As such the information rendered in the configuration is kept to a minimum.

### HTTP Request

`GET /go/api/config/pipeline_groups`

### Returns

A list of pipeline groups, pipelines in each group, stages and materials in each pipeline.
