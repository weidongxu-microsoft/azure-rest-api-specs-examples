```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.VirtualMachineRunCommandScriptSource;
import com.azure.resourcemanager.compute.models.VirtualMachineRunCommandUpdate;

/** Samples for VirtualMachineScaleSetVMRunCommands Update. */
public final class UpdateVirtualMachineScaleSetVMRunCommands {
    /*
     * operationId: VirtualMachineScaleSetVMRunCommands_Update
     * api-version: 2021-04-01
     * x-ms-examples: Update VirtualMachineScaleSet VM run command.
     */
    /**
     * Sample code: Update VirtualMachineScaleSet VM run command.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void updateVirtualMachineScaleSetVMRunCommand(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSetVMRunCommands()
            .update(
                "myResourceGroup",
                "myvmScaleSet",
                "0",
                "myRunCommand",
                new VirtualMachineRunCommandUpdate()
                    .withSource(
                        new VirtualMachineRunCommandScriptSource().withScript("Write-Host Script Source Updated!")),
                Context.NONE);
    }
}
```