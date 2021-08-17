```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.VirtualMachineRunCommandScriptSource;
import com.azure.resourcemanager.compute.models.VirtualMachineRunCommandUpdate;

/** Samples for VirtualMachineRunCommands Update. */
public final class UpdateRunCommand {
    /*
     * operationId: VirtualMachineRunCommands_Update
     * api-version: 2021-04-01
     * x-ms-examples: Update a run command.
     */
    /**
     * Sample code: Update a run command.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void updateARunCommand(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineRunCommands()
            .update(
                "myResourceGroup",
                "myVM",
                "myRunCommand",
                new VirtualMachineRunCommandUpdate()
                    .withSource(
                        new VirtualMachineRunCommandScriptSource().withScript("Write-Host Script Source Updated!")),
                Context.NONE);
    }
}
```