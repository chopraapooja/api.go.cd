## Get all artifacts

```shell
$ curl 'https://ci.example.com/go/files/PipelineName/541/StageName/1/JobName.json' \
      -u 'username:password'
```

> The above command returns JSON structured like this:

```http
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
```

```json
{
    "name": "cruise-output",
    "url": "https://ci.example.com/go/files/PipelineName/541/StageName/1/JobName/cruise-output",
    "type": "folder",
    "files": [
      {
        "name": "console.log",
        "url": "https://ci.example.com/go/files/PipelineName/541/StageName/1/JobName/cruise-output/console.log",
        "type": "file"
      },
      {
        "name": "md5.checksum",
        "url": "https://ci.example.com/go/files/PipelineName/541/StageName/1/JobName/cruise-output/md5.checksum",
        "type": "file"
      }
    ]
  }
```

Lists all available artifacts in a job.

### HTTP Request

`GET /go/files/:pipeline_name/:pipeline_counter/:stage_name/:stage_counter/:job_name.json`

### Returns

An array of [artifact objects](#the-artifact-object).
