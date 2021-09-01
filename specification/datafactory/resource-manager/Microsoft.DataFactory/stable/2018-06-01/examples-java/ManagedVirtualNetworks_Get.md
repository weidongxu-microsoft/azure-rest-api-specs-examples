Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for ManagedVirtualNetworks Get. */
public final class Main {
    /*
     * operationId: ManagedVirtualNetworks_Get
     * api-version: 2018-06-01
     * x-ms-examples: ManagedVirtualNetworks_Get
     */
    /**
     * Sample code: ManagedVirtualNetworks_Get.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void managedVirtualNetworksGet(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .managedVirtualNetworks()
            .getWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "exampleManagedVirtualNetworkName", null, Context.NONE);
    }
}
```
