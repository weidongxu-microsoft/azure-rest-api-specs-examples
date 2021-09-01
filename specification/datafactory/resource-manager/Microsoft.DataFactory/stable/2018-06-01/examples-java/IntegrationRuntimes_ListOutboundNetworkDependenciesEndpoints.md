Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes ListOutboundNetworkDependenciesEndpoints. */
public final class Main {
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
