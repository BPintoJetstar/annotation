      ,com.jcabi;resolution:=optional,
                            ,org.apache.ibatis

                            org.apache.openjpa.enhance;resolution:=optional,
                            org.apache.openjpa.util;resolution:=optional,
                            org.osgi.framework,*;resolution:=optional,
                            *;resolution:=optional
                            
                            mysql  Ver 14.14 Distrib 5.7.24, for Linux (x86_64) using  EditLine wrapper


# ESSENTIALS

**OPENJPA**
- `features:install openjpa/2.3.0`

**HTTP4**
- features:install camel-http4

**JPA**
- install -s mvn:org.apache.geronimo.specs/geronimo-jpa_2.0_spec/1.1 

**DATASOURCE**
- [see this post ](https://stackoverflow.com/questions/44528974/fuse-6-3-dbcp-basic-datasource)

**H2**
- install -s mvn:com.h2database/h2/1.4.196

**MYSQL**
- install wrap:mvn:mysql/mysql-connector-java/5.1.24

**DBPCH**
- install mvn:org.apache.servicemix.bundles/org.apache.servicemix.bundles.commons-dbcp/1.4_3


# FEATURES INSTALL 
```
<?xml version="1.0" encoding="UTF-8"?>
<features name="CustomRepository">
</features>
```
### Register the file 
features:addUrl file:C:/Projects/features.xml

### Refresh
features:refreshUrl

### List
features:list
features:listUrl

### Deploy
features:install example-camel-bundle

# PERSISTENT-ID
````
<blueprint
    xmlns="http://www.osgi.org/xmlns/blueprint/v1.0.0"
 xmlns:cm="http://aries.apache.org/blueprint/xmlns/blueprint-cm/v1.1.0"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    ... >
    ...
    <cm:property-placeholder persistent-id="org.fusesource.example">
        <cm:default-properties>
            <cm:property name="prefix" value="Blueprint-Example"/>
        </cm:default-properties>
    </cm:property-placeholder>

    <bean id="myTransform" class="org.example.camel.MyTransform">
        <property name="prefix" value="${prefix}" />
    </bean>

</blueprint>
````
