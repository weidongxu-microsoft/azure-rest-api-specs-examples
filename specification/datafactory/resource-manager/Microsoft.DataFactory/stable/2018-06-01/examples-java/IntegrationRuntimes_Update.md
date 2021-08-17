```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.IntegrationRuntimeAutoUpdate;
import com.azure.resourcemanager.datafactory.models.IntegrationRuntimeResource;

/** Samples for IntegrationRuntimes Update. */
public final class IntegrationRuntimesUpdate {
    /*
     * operationId: IntegrationRuntimes_Update
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_Update
     */
    /**
     * Sample code: IntegrationRuntimes_Update.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesUpdate(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        IntegrationRuntimeResource resource =
            manager
                .integrationRuntimes()
                .getWithResponse(
                    "exampleResourceGroup", "exampleFactoryName", "exampleIntegrationRuntime", null, Context.NONE)
                .getValue();
        resource.update().withAutoUpdate(IntegrationRuntimeAutoUpdate.OFF).withUpdateDelayOffset("\"PT3H\"").apply();
    }
}
```