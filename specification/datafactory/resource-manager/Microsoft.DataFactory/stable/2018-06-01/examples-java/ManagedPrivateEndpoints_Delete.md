Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for ManagedPrivateEndpoints Delete. */
public final class Main {
    /*
     * operationId: ManagedPrivateEndpoints_Delete
     * api-version: 2018-06-01
     * x-ms-examples: ManagedVirtualNetworks_Delete
     */
    /**
     * Sample code: ManagedVirtualNetworks_Delete.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void managedVirtualNetworksDelete(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .managedPrivateEndpoints()
            .deleteWithResponse(
                "exampleResourceGroup",
                "exampleFactoryName",
                "exampleManagedVirtualNetworkName",
                "exampleManagedPrivateEndpointName",
                Context.NONE);
    }
}
```
