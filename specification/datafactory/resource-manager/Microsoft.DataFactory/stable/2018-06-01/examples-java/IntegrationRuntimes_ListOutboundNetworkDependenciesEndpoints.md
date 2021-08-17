```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes ListOutboundNetworkDependenciesEndpoints. */
public final
class IntegrationRuntimesListOutboundNetworkDependenciesEndpoints {
    /*
     * operationId: IntegrationRuntimes_ListOutboundNetworkDependenciesEndpoints
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_OutboundNetworkDependenciesEndpoints
     */
    /**
     * Sample code: IntegrationRuntimes_OutboundNetworkDependenciesEndpoints.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesOutboundNetworkDependenciesEndpoints(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimes()
            .listOutboundNetworkDependenciesEndpointsWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "exampleIntegrationRuntime", Context.NONE);
    }
}
```