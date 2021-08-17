```java
import com.azure.core.util.Context;

/** Samples for VirtualMachines ListByLocation. */
public final
class ListVirtualMachinesInASubscriptionByLocation {
    /*
     * operationId: VirtualMachines_ListByLocation
     * api-version: 2021-04-01
     * x-ms-examples: Lists all the virtual machines under the specified subscription for the specified location.
     */
    /**
     * Sample code: Lists all the virtual machines under the specified subscription for the specified location.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listsAllTheVirtualMachinesUnderTheSpecifiedSubscriptionForTheSpecifiedLocation(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure.virtualMachines().manager().serviceClient().getVirtualMachines().listByLocation("eastus", Context.NONE);
    }
}
```