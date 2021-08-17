```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSetVMs Delete. */
public final class ForceDeleteVirtualMachineScaleSetVM {
    /*
     * operationId: VirtualMachineScaleSetVMs_Delete
     * api-version: 2021-04-01
     * x-ms-examples: Force Delete a virtual machine from a VM scale set.
     */
    /**
     * Sample code: Force Delete a virtual machine from a VM scale set.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void forceDeleteAVirtualMachineFromAVMScaleSet(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSetVMs()
            .delete("myResourceGroup", "myvmScaleSet", "0", true, Context.NONE);
    }
}
```