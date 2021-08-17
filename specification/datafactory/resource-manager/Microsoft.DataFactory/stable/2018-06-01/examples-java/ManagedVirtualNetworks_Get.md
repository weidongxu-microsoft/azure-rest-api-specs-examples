```java
import com.azure.core.util.Context;

/** Samples for ManagedVirtualNetworks Get. */
public final class ManagedVirtualNetworksGet {
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