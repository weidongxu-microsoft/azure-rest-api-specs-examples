```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes Delete. */
public final class IntegrationRuntimesDelete {
    /*
     * operationId: IntegrationRuntimes_Delete
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_Delete
     */
    /**
     * Sample code: IntegrationRuntimes_Delete.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesDelete(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimes()
            .deleteWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "exampleIntegrationRuntime", Context.NONE);
    }
}
```