```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineRunCommands List. */
public final class VirtualMachineRunCommandList {
    /*
     * operationId: VirtualMachineRunCommands_List
     * api-version: 2021-04-01
     * x-ms-examples: VirtualMachineRunCommandList
     */
    /**
     * Sample code: VirtualMachineRunCommandList.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void virtualMachineRunCommandList(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineRunCommands()
            .list("SoutheastAsia", Context.NONE);
    }
}
```