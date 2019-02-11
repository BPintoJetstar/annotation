# ESSENTIALS

**UNINSTALL**
- uninstall canonical-model soap-channel db-translator  order-manager cbr splitter suppliera-translator supplierb-translator supplierc-translator datasource

**OPENJPA**
- `features:install openjpa/2.3.0`

**HTTP4**
- features:install camel-http4

**JPA**
- install -s mvn:org.apache.geronimo.specs/geronimo-jpa_2.0_spec/1.1 


**H2**
- install -s mvn:com.h2database/h2/1.4.196

**MYSQL**
- install wrap:mvn:mysql/mysql-connector-java/5.1.24

**DBPCH**
- install mvn:org.apache.servicemix.bundles/org.apache.servicemix.bundles.commons-dbcp/1.4_3

**PAX**
- features:addurl mvn:org.ops4j.pax.jdbc/pax-jdbc-features/1.1.0/xml/features
- features:install pax-jdbc-config pax-jdbc-mysql pax-jdbc-pool-aries transaction 

# FEATURE DEPLOY 

### Sample
```
<?xml version="1.0" encoding="UTF-8"?>

<features name="features-repository">

    <feature name="goodbooze-features" version="1.0-SNAPSHOT">
        <feature version="1.0-SNAPSHOT">canonical-model</feature>
        <feature version="1.0-SNAPSHOT">soap-channel</feature>
    </feature>

    <feature name="canonical-model" version="1.0-SNAPSHOT">
        <bundle>mvn:au.com.marlo.goodbooze/canonical-model/1.0-SNAPSHOT</bundle>
    </feature>

    <feature name="soap-channel" version="1.0-SNAPSHOT">
        <bundle>mvn:au.com.marlo.goodbooze/soap-channel/1.0-SNAPSHOT</bundle>
        <feature version="1.0-SNAPSHOT">canonical-model</feature>
    </feature>
</features>
```

### Register the xml 
features:addUrl mvn:[groupID]/[arctifacID]/[version]/xml/[feature_file_name]

### Refresh
Always remember to refresh:

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
# DATASOURCE
- [see this post ](https://stackoverflow.com/questions/44528974/fuse-6-3-dbcp-basic-datasource)
# COMMONS ERROS

```
Caused by: java.lang.NoClassDefFoundError: Could not initialize class au.com.marlo.db.translator.crud.SupplierOrderCRUD
```
Solve: Remove the Log class. 
