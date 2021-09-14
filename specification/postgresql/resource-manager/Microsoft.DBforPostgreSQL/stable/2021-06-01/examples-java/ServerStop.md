Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-postgresqlflexibleserver_1.0.0-beta.3/sdk/postgresqlflexibleserver/azure-resourcemanager-postgresqlflexibleserver/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Servers Stop. */
public final class Main {
    /*
     * operationId: Servers_Stop
     * api-version: 2021-06-01
     * x-ms-examples: ServerStop
     */
    /**
     * Sample code: ServerStop.
     *
     * @param manager Entry point to PostgreSqlManager.
     */
    public static void serverStop(com.azure.resourcemanager.postgresqlflexibleserver.PostgreSqlManager manager) {
        manager.servers().stop("testrg", "testserver", Context.NONE);
    }
}
```
