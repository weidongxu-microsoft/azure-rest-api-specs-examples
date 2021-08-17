```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSetVMRunCommands Delete. */
public final class DeleteVirtualMachineScaleSetVMRunCommands {
    /*
     * operationId: VirtualMachineScaleSetVMRunCommands_Delete
     * api-version: 2021-04-01
     * x-ms-examples: Delete VirtualMachineScaleSet VM run command.
     */
    /**
     * Sample code: Delete VirtualMachineScaleSet VM run command.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteVirtualMachineScaleSetVMRunCommand(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSetVMRunCommands()
            .delete("myResourceGroup", "myvmScaleSet", "0", "myRunCommand", Context.NONE);
    }
}
```