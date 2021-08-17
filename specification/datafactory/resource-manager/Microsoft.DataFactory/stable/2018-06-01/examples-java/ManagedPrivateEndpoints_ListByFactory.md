```java
import com.azure.core.util.Context;

/** Samples for ManagedPrivateEndpoints ListByFactory. */
public final class ManagedPrivateEndpointsListByFactory {
    /*
     * operationId: ManagedPrivateEndpoints_ListByFactory
     * api-version: 2018-06-01
     * x-ms-examples: ManagedPrivateEndpoints_ListByFactory
     */
    /**
     * Sample code: ManagedPrivateEndpoints_ListByFactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void managedPrivateEndpointsListByFactory(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .managedPrivateEndpoints()
            .listByFactory(
                "exampleResourceGroup", "exampleFactoryName", "exampleManagedVirtualNetworkName", Context.NONE);
    }
}
```