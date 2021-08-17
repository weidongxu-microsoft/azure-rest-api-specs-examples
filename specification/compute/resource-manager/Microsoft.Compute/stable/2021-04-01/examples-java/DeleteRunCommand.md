```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineRunCommands Delete. */
public final class DeleteRunCommand {
    /*
     * operationId: VirtualMachineRunCommands_Delete
     * api-version: 2021-04-01
     * x-ms-examples: Delete a run command.
     */
    /**
     * Sample code: Delete a run command.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteARunCommand(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineRunCommands()
            .delete("myResourceGroup", "myVM", "myRunCommand", Context.NONE);
    }
}
```