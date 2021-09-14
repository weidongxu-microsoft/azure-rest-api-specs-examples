Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ManagedPrivateEndpoints ListByFactory. */
public final class Main {
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
