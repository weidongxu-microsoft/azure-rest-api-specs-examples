Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-postgresqlflexibleserver_1.0.0-beta.3/sdk/postgresqlflexibleserver/azure-resourcemanager-postgresqlflexibleserver/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Configurations ListByServer. */
public final class Main {
    /*
     * operationId: Configurations_ListByServer
     * api-version: 2021-06-01
     * x-ms-examples: ConfigurationList
     */
    /**
     * Sample code: ConfigurationList.
     *
     * @param manager Entry point to PostgreSqlManager.
     */
    public static void configurationList(com.azure.resourcemanager.postgresqlflexibleserver.PostgreSqlManager manager) {
        manager.configurations().listByServer("testrg", "testserver", Context.NONE);
    }
}
```
