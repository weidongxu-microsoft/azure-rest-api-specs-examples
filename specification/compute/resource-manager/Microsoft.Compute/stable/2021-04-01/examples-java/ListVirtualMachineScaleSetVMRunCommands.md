```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSetVMRunCommands List. */
public final class ListVirtualMachineScaleSetVMRunCommands {
    /*
     * operationId: VirtualMachineScaleSetVMRunCommands_List
     * api-version: 2021-04-01
     * x-ms-examples: List run commands in Vmss instance.
     */
    /**
     * Sample code: List run commands in Vmss instance.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listRunCommandsInVmssInstance(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSetVMRunCommands()
            .list("myResourceGroup", "myvmScaleSet", "0", null, Context.NONE);
    }
}
```