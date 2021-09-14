Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-synapse_1.0.0-beta.2/sdk/synapse/azure-resourcemanager-synapse/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for SqlPools Pause. */
public final class Main {
    /*
     * x-ms-original-file: specification/synapse/resource-manager/Microsoft.Synapse/stable/2021-06-01/examples/PauseSqlPool.json
     */
    /**
     * Sample code: Pause a SQL Analytics pool.
     *
     * @param manager Entry point to SynapseManager.
     */
    public static void pauseASQLAnalyticsPool(com.azure.resourcemanager.synapse.SynapseManager manager) {
        manager.sqlPools().pause("Default-SQL-SouthEastAsia", "testsvr", "testdwdb", Context.NONE);
    }
}
```