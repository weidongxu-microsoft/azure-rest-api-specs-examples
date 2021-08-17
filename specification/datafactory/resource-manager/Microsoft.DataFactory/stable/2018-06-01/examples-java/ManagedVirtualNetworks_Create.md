```java
import com.azure.resourcemanager.datafactory.models.ManagedVirtualNetwork;

/** Samples for ManagedVirtualNetworks CreateOrUpdate. */
public final class ManagedVirtualNetworksCreate {
    /*
     * operationId: ManagedVirtualNetworks_CreateOrUpdate
     * api-version: 2018-06-01
     * x-ms-examples: ManagedVirtualNetworks_Create
     */
    /**
     * Sample code: ManagedVirtualNetworks_Create.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void managedVirtualNetworksCreate(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .managedVirtualNetworks()
            .define("exampleManagedVirtualNetworkName")
            .withExistingFactory("exampleResourceGroup", "exampleFactoryName")
            .withProperties(new ManagedVirtualNetwork())
            .create();
    }
}
```