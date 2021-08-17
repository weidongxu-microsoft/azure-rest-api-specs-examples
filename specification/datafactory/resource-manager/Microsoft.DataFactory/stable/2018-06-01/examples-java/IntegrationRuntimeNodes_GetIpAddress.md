```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimeNodes GetIpAddress. */
public final class IntegrationRuntimeNodesGetIpAddress {
    /*
     * operationId: IntegrationRuntimeNodes_GetIpAddress
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimeNodes_GetIpAddress
     */
    /**
     * Sample code: IntegrationRuntimeNodes_GetIpAddress.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimeNodesGetIpAddress(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimeNodes()
            .getIpAddressWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "exampleIntegrationRuntime", "Node_1", Context.NONE);
    }
}
```