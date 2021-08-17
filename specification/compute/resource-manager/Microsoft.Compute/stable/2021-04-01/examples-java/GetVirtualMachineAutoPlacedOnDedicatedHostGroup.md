```java
import com.azure.core.util.Context;

/** Samples for VirtualMachines GetByResourceGroup. */
public final
class GetVirtualMachineAutoPlacedOnDedicatedHostGroup {
    /*
     * operationId: VirtualMachines_Get
     * api-version: 2021-04-01
     * x-ms-examples: Get a virtual machine placed on a dedicated host group through automatic placement
     */
    /**
     * Sample code: Get a virtual machine placed on a dedicated host group through automatic placement.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAVirtualMachinePlacedOnADedicatedHostGroupThroughAutomaticPlacement(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachines()
            .getByResourceGroupWithResponse("myResourceGroup", "myVM", null, Context.NONE);
    }
}
```