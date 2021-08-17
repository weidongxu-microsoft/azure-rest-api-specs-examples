```java
import com.azure.core.util.Context;

/** Samples for ManagedPrivateEndpoints Get. */
public final class ManagedPrivateEndpointsGet {
    /*
     * operationId: ManagedPrivateEndpoints_Get
     * api-version: 2018-06-01
     * x-ms-examples: ManagedPrivateEndpoints_Get
     */
    /**
     * Sample code: ManagedPrivateEndpoints_Get.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void managedPrivateEndpointsGet(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .managedPrivateEndpoints()
            .getWithResponse(
                "exampleResourceGroup",
                "exampleFactoryName",
                "exampleManagedVirtualNetworkName",
                "exampleManagedPrivateEndpointName",
                null,
                Context.NONE);
    }
}
```