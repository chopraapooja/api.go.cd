## Get repository modification diff 

```shell
$ curl 'https://ci.example.com/go/api/config/diff/d2f9091145e2e4b3b22d938c4819610467ae20c1/f27b48594645c9f15f55bb56d0100dd60e4cbacc' \
      -u 'username:password' 
```

> The above command returns the following response:

```http
HTTP/1.1 200 OK
Content-Type: text/plain; charset=utf-8
```

```diff
@@ -29,7 +29,7 @@
           <job name="up42_job">
             <tasks>
               <exec command="sleep">
-                <arg>40000</arg>
+                <arg>100</arg>
                 <runif status="passed" />
               </exec>
             </tasks>
```

Gets the diff between two config repository modifications.

### HTTP Request

`GET /go/api/config/:from_commit_sha/:to_commit_sha`


### Returns

The diff between two config repo modifications.
