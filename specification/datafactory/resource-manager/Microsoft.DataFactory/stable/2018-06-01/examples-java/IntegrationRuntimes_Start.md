```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes Start. */
public final class IntegrationRuntimesStart {
    /*
     * operationId: IntegrationRuntimes_Start
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_Start
     */
    /**
     * Sample code: IntegrationRuntimes_Start.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesStart(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimes()
            .start("exampleResourceGroup", "exampleFactoryName", "exampleManagedIntegrationRuntime", Context.NONE);
    }
}
```