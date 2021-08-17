```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes SyncCredentials. */
public final class IntegrationRuntimesSyncCredentials {
    /*
     * operationId: IntegrationRuntimes_SyncCredentials
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_SyncCredentials
     */
    /**
     * Sample code: IntegrationRuntimes_SyncCredentials.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesSyncCredentials(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimes()
            .syncCredentialsWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "exampleIntegrationRuntime", Context.NONE);
    }
}
```