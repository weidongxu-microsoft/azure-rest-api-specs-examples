```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSetVMRunCommands Get. */
public final class GetVirtualMachineScaleSetVMRunCommands {
    /*
     * operationId: VirtualMachineScaleSetVMRunCommands_Get
     * api-version: 2021-04-01
     * x-ms-examples: Get VirtualMachineScaleSet VM run commands.
     */
    /**
     * Sample code: Get VirtualMachineScaleSet VM run commands.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getVirtualMachineScaleSetVMRunCommands(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSetVMRunCommands()
            .getWithResponse("myResourceGroup", "myvmScaleSet", "0", "myRunCommand", null, Context.NONE);
    }
}
```