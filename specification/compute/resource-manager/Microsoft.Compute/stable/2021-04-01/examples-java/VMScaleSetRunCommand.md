```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.RunCommandInput;
import java.util.Arrays;

/** Samples for VirtualMachineScaleSetVMs RunCommand. */
public final class VMScaleSetRunCommand {
    /*
     * operationId: VirtualMachineScaleSetVMs_RunCommand
     * api-version: 2021-04-01
     * x-ms-examples: VirtualMachineScaleSetVMs_RunCommand
     */
    /**
     * Sample code: VirtualMachineScaleSetVMs_RunCommand.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void virtualMachineScaleSetVMsRunCommand(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSetVMs()
            .runCommand(
                "myResourceGroup",
                "myVirtualMachineScaleSet",
                "0",
                new RunCommandInput()
                    .withCommandId("RunPowerShellScript")
                    .withScript(Arrays.asList("Write-Host Hello World!")),
                Context.NONE);
    }
}
```