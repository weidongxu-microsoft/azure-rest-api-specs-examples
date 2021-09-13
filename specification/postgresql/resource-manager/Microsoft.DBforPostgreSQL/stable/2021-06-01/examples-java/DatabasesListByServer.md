Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-postgresqlflexibleserver_1.0.0-beta.3/sdk/postgresqlflexibleserver/azure-resourcemanager-postgresqlflexibleserver/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Databases ListByServer. */
public final class Main {
    /*
     * operationId: Databases_ListByServer
     * api-version: 2021-06-01
     * x-ms-examples: List databases in a server
     */
    /**
     * Sample code: List databases in a server.
     *
     * @param manager Entry point to PostgreSqlManager.
     */
    public static void listDatabasesInAServer(
        com.azure.resourcemanager.postgresqlflexibleserver.PostgreSqlManager manager) {
        manager.databases().listByServer("TestGroup", "testserver", Context.NONE);
    }
}
```
