```java
import com.azure.core.util.Context;

/** Samples for VirtualMachines InstanceView. */
public final
class GetVirtualMachineInstanceViewAutoPlacedOnDedicatedHostGroup {
    /*
     * operationId: VirtualMachines_InstanceView
     * api-version: 2021-04-01
     * x-ms-examples: Get instance view of a virtual machine placed on a dedicated host group through automatic placement.
     */
    /**
     * Sample code: Get instance view of a virtual machine placed on a dedicated host group through automatic placement.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getInstanceViewOfAVirtualMachinePlacedOnADedicatedHostGroupThroughAutomaticPlacement(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachines()
            .instanceViewWithResponse("myResourceGroup", "myVM", Context.NONE);
    }
}
```