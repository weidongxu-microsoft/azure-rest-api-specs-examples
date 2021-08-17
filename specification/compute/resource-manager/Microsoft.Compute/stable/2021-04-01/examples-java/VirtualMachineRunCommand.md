```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.RunCommandInput;

/** Samples for VirtualMachines RunCommand. */
public final class VirtualMachineRunCommand {
    /*
     * operationId: VirtualMachines_RunCommand
     * api-version: 2021-04-01
     * x-ms-examples: VirtualMachineRunCommand
     */
    /**
     * Sample code: VirtualMachineRunCommand.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void virtualMachineRunCommand(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachines()
            .runCommand(
                "crptestar98131", "vm3036", new RunCommandInput().withCommandId("RunPowerShellScript"), Context.NONE);
    }
}
```