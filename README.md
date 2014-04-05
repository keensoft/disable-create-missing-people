disable-create-missing-people
=============================

ALFRESCO · Disable createMissingPeople property on PersonService.

Extracted from Alfresco 4.2.c alfresco/tomcat/webapps/alfresco/WEB-INF/classes/alfresco/authentication-services-context.xml

```
<!-- Some authentication mechanisms may need to create people -->
<!-- in the repository on demand. This enables that feature. -->
<!-- If dsiabled an error will be generated for missing -->
<!-- people. If enabled then a person will be created and -->
<!-- persisted. -->
<!-- Valid values are -->
<!-- ${server.transaction.allow-writes} -->
<!-- false -->
<property name="createMissingPeople">
<value>${server.transaction.allow-writes}
</value>
</property>
```

You can include this Alfresco repo AMP in any Alfresco 4.X CE / EE in order to set this property to false. This avoids you to change source from Alfresco product.

Note
====
On Alfresco 4.2.d CE and Alfresco 4.2 EE there is a new called "create.missing.people" which allows to set the desired behaviour without impacting any other functionality.
