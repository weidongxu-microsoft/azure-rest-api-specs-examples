```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineRunCommands ListByVirtualMachine. */
public final class ListRunCommandsInVM {
    /*
     * operationId: VirtualMachineRunCommands_ListByVirtualMachine
     * api-version: 2021-04-01
     * x-ms-examples: List run commands in a Virtual Machine.
     */
    /**
     * Sample code: List run commands in a Virtual Machine.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listRunCommandsInAVirtualMachine(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineRunCommands()
            .listByVirtualMachine("myResourceGroup", "myVM", null, Context.NONE);
    }
}
```