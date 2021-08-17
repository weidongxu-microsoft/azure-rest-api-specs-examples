```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineRunCommands Get. */
public final class VirtualMachineRunCommandGet {
    /*
     * operationId: VirtualMachineRunCommands_Get
     * api-version: 2021-04-01
     * x-ms-examples: VirtualMachineRunCommandGet
     */
    /**
     * Sample code: VirtualMachineRunCommandGet.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void virtualMachineRunCommandGet(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineRunCommands()
            .getWithResponse("SoutheastAsia", "RunPowerShellScript", Context.NONE);
    }
}
```