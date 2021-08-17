```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineRunCommands GetByVirtualMachine. */
public final class GetRunCommand {
    /*
     * operationId: VirtualMachineRunCommands_GetByVirtualMachine
     * api-version: 2021-04-01
     * x-ms-examples: Get a run command.
     */
    /**
     * Sample code: Get a run command.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getARunCommand(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineRunCommands()
            .getByVirtualMachineWithResponse("myResourceGroup", "myVM", "myRunCommand", null, Context.NONE);
    }
}
```