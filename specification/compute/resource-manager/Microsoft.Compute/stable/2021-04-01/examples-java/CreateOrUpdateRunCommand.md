```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.VirtualMachineRunCommandInner;
import com.azure.resourcemanager.compute.models.RunCommandInputParameter;
import com.azure.resourcemanager.compute.models.VirtualMachineRunCommandScriptSource;
import java.util.Arrays;

/** Samples for VirtualMachineRunCommands CreateOrUpdate. */
public final class CreateOrUpdateRunCommand {
    /*
     * operationId: VirtualMachineRunCommands_CreateOrUpdate
     * api-version: 2021-04-01
     * x-ms-examples: Create or update a run command.
     */
    /**
     * Sample code: Create or update a run command.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createOrUpdateARunCommand(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineRunCommands()
            .createOrUpdate(
                "myResourceGroup",
                "myVM",
                "myRunCommand",
                new VirtualMachineRunCommandInner()
                    .withLocation("West US")
                    .withSource(new VirtualMachineRunCommandScriptSource().withScript("Write-Host Hello World!"))
                    .withParameters(
                        Arrays
                            .asList(
                                new RunCommandInputParameter().withName("param1").withValue("value1"),
                                new RunCommandInputParameter().withName("param2").withValue("value2")))
                    .withAsyncExecution(false)
                    .withRunAsUser("user1")
                    .withRunAsPassword("<runAsPassword>")
                    .withTimeoutInSeconds(3600),
                Context.NONE);
    }
}
```