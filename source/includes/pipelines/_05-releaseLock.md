## Releasing a pipeline lock

```shell

$ curl 'http://ci.example.com/go/api/pipelines/pipeline1/releaseLock' \
       -u 'username:password'
       -X POST
```

> The above command returns the following response:

```http
HTTP/1.1 200 OK
Content-Type: text/html; charset=utf-8
pipeline lock released for pipeline1
```


The releasing a pipeline lock  allows user to release a lock on a pipeline so that you can start up a new instance without having to wait for the earlier instance to finish.
<aside class="notice">
 A pipeline lock can only be released when a pipeline is locked, AND there is no running instance of the pipeline.
</aside>

### HTTP Request

`GET /go/pipelines/:pipeline_name/releaseLock`

### Returns

A text confirmation.