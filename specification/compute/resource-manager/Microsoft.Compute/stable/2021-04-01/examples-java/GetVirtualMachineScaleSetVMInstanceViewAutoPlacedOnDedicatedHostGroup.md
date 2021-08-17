```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSetVMs GetInstanceView. */
public final
class GetVirtualMachineScaleSetVMInstanceViewAutoPlacedOnDedicatedHostGroup {
    /*
     * operationId: VirtualMachineScaleSetVMs_GetInstanceView
     * api-version: 2021-04-01
     * x-ms-examples: Get instance view of a virtual machine from a VM scale set placed on a dedicated host group through automatic placement.
     */
    /**
     * Sample code: Get instance view of a virtual machine from a VM scale set placed on a dedicated host group through
     * automatic placement.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void
        getInstanceViewOfAVirtualMachineFromAVMScaleSetPlacedOnADedicatedHostGroupThroughAutomaticPlacement(
            com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSetVMs()
            .getInstanceViewWithResponse("myResourceGroup", "myVirtualMachineScaleSet", "0", Context.NONE);
    }
}
```