## Get configuration 

```shell
$ curl 'https://ci.example.com/go/api/admin/config/5059cf548db9ea2d1b9192b45529ccf0.xml' \
      -u 'username:password' 
```

> The above command returns the contents of the config file

```xml
<?xml version="1.0" encoding="utf-8"?>
<cruise 
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xsi:noNamespaceSchemaLocation="cruise-config.xsd" 
    schemaVersion="75">
  <server serverId="9C0C0282-A554-457D-A0F8-9CF8A754B4AB">
    <security>
      <passwordFile path="/etc/go/password.properties" />
    </security>
  </server>
  <pipelines group="defaultGroup" />
</cruise>
```

Gets the configuration with the specified version.

### HTTP Request

`GET /go/api/admin/config/:commit_sha.xml`

**Other convenience APIs**

`GET /go/api/admin/config/config.xml`
    
    or
    
`GET /go/api/admin/config/current.xml`

<aside class="notice">
  <strong>Note:</strong> <code>config.xml</code> or <code>current.xml</code> allows retrieval of current configuration without passing in the commit sha value.
</aside>

### Returns

The contents of the configuration file with the specified revision. 
