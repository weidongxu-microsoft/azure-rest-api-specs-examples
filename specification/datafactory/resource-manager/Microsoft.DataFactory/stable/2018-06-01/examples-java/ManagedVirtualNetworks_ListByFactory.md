```java
import com.azure.core.util.Context;

/** Samples for ManagedVirtualNetworks ListByFactory. */
public final class ManagedVirtualNetworksListByFactory {
    /*
     * operationId: ManagedVirtualNetworks_ListByFactory
     * api-version: 2018-06-01
     * x-ms-examples: ManagedVirtualNetworks_ListByFactory
     */
    /**
     * Sample code: ManagedVirtualNetworks_ListByFactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void managedVirtualNetworksListByFactory(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.managedVirtualNetworks().listByFactory("exampleResourceGroup", "exampleFactoryName", Context.NONE);
    }
}
```