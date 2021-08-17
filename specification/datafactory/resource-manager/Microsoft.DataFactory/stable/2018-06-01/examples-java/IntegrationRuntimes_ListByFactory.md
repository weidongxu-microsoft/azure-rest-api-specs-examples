```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes ListByFactory. */
public final class IntegrationRuntimesListByFactory {
    /*
     * operationId: IntegrationRuntimes_ListByFactory
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_ListByFactory
     */
    /**
     * Sample code: IntegrationRuntimes_ListByFactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesListByFactory(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.integrationRuntimes().listByFactory("exampleResourceGroup", "exampleFactoryName", Context.NONE);
    }
}
```