# ESSENTIALS

OPENJPA

- features:install openjpa

JPA
- install -s mvn:org.apache.geronimo.specs/geronimo-jpa_2.0_spec/1.1 

DATASOURCE
- [see this post ](https://stackoverflow.com/questions/44528974/fuse-6-3-dbcp-basic-datasource)

H2
- install -s mvn:com.h2database/h2/1.4.196

MYSQL
- install wrap:mvn:mysql/mysql-connector-java/5.1.24

DBPCH
- install mvn:org.apache.servicemix.bundles/org.apache.servicemix.bundles.commons-dbcp/1.4_3

PAX FEATURES
- feature:repo-add mvn:org.ops4j.pax.jdbc/pax-jdbc-features/1.1.0/xml/features

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
