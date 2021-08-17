```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSets GetByResourceGroup. */
public final
class GetVirtualMachineScaleSetAutoPlacedOnDedicatedHostGroup {
    /*
     * operationId: VirtualMachineScaleSets_Get
     * api-version: 2021-04-01
     * x-ms-examples: Get a virtual machine scale set placed on a dedicated host group through automatic placement.
     */
    /**
     * Sample code: Get a virtual machine scale set placed on a dedicated host group through automatic placement.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAVirtualMachineScaleSetPlacedOnADedicatedHostGroupThroughAutomaticPlacement(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSets()
            .getByResourceGroupWithResponse("myResourceGroup", "myVirtualMachineScaleSet", null, Context.NONE);
    }
}
```