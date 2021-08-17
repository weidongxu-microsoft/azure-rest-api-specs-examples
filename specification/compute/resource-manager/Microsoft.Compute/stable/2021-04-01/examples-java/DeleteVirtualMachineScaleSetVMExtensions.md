```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSetVMExtensions Delete. */
public final class DeleteVirtualMachineScaleSetVMExtensions {
    /*
     * operationId: VirtualMachineScaleSetVMExtensions_Delete
     * api-version: 2021-04-01
     * x-ms-examples: Delete VirtualMachineScaleSet VM extension.
     */
    /**
     * Sample code: Delete VirtualMachineScaleSet VM extension.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteVirtualMachineScaleSetVMExtension(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSetVMExtensions()
            .delete("myResourceGroup", "myvmScaleSet", "0", "myVMExtension", Context.NONE);
    }
}
```