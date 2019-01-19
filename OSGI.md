# FEATURES ESSENTIALS

JBossFuse:karaf@root> features:install camel-blueprint

# FEATURES INSTALL 
```
<?xml version="1.0" encoding="UTF-8"?>
<features name="CustomRepository">
</features>
```
### Register the file 
features:addUrl file:C:/Projects/features.xml

### Refresh
JBossFuse:karaf@root> features:refreshUrl

### List
JBossFuse:karaf@root> features:list
JBossFuse:karaf@root> features:listUrl


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
