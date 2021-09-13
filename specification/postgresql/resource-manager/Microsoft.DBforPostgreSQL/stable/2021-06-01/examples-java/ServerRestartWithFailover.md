Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-postgresqlflexibleserver_1.0.0-beta.3/sdk/postgresqlflexibleserver/azure-resourcemanager-postgresqlflexibleserver/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.postgresqlflexibleserver.models.FailoverMode;
import com.azure.resourcemanager.postgresqlflexibleserver.models.RestartParameter;

/** Samples for Servers Restart. */
public final class Main {
    /*
     * operationId: Servers_Restart
     * api-version: 2021-06-01
     * x-ms-examples: ServerRestartWithFailover
     */
    /**
     * Sample code: ServerRestartWithFailover.
     *
     * @param manager Entry point to PostgreSqlManager.
     */
    public static void serverRestartWithFailover(
        com.azure.resourcemanager.postgresqlflexibleserver.PostgreSqlManager manager) {
        manager
            .servers()
            .restart(
                "testrg",
                "testserver",
                new RestartParameter().withRestartWithFailover(true).withFailoverMode(FailoverMode.FORCED_FAILOVER),
                Context.NONE);
    }
}
```
