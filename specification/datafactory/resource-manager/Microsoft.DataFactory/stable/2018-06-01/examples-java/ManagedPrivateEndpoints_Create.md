```java
import com.azure.resourcemanager.datafactory.models.ManagedPrivateEndpoint;
import java.util.Arrays;

/** Samples for ManagedPrivateEndpoints CreateOrUpdate. */
public final class ManagedPrivateEndpointsCreate {
    /*
     * operationId: ManagedPrivateEndpoints_CreateOrUpdate
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
            .managedPrivateEndpoints()
            .define("exampleManagedPrivateEndpointName")
            .withExistingManagedVirtualNetwork(
                "exampleResourceGroup", "exampleFactoryName", "exampleManagedVirtualNetworkName")
            .withProperties(
                new ManagedPrivateEndpoint()
                    .withFqdns(Arrays.asList())
                    .withGroupId("blob")
                    .withPrivateLinkResourceId(
                        "/subscriptions/12345678-1234-1234-1234-12345678abc/resourceGroups/exampleResourceGroup/providers/Microsoft.Storage/storageAccounts/exampleBlobStorage"))
            .create();
    }
}
```