```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes Stop. */
public final class IntegrationRuntimesStop {
    /*
     * operationId: IntegrationRuntimes_Stop
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_Stop
     */
    /**
     * Sample code: IntegrationRuntimes_Stop.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesStop(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimes()
            .stop("exampleResourceGroup", "exampleFactoryName", "exampleManagedIntegrationRuntime", Context.NONE);
    }
}
```