```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSets ListByLocation. */
public final
class ListVirtualMachineScaleSetsInASubscriptionByLocation {
    /*
     * operationId: VirtualMachineScaleSets_ListByLocation
     * api-version: 2021-04-01
     * x-ms-examples: Lists all the VM scale sets under the specified subscription for the specified location.
     */
    /**
     * Sample code: Lists all the VM scale sets under the specified subscription for the specified location.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listsAllTheVMScaleSetsUnderTheSpecifiedSubscriptionForTheSpecifiedLocation(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSets()
            .listByLocation("eastus", Context.NONE);
    }
}
```