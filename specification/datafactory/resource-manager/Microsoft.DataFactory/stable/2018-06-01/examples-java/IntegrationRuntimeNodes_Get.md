```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimeNodes Get. */
public final class IntegrationRuntimeNodesGet {
    /*
     * operationId: IntegrationRuntimeNodes_Get
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimeNodes_Get
     */
    /**
     * Sample code: IntegrationRuntimeNodes_Get.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimeNodesGet(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimeNodes()
            .getWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "exampleIntegrationRuntime", "Node_1", Context.NONE);
    }
}
```