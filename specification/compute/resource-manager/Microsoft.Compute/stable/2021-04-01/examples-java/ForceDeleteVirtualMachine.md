```java
import com.azure.core.util.Context;

/** Samples for VirtualMachines Delete. */
public final class ForceDeleteVirtualMachine {
    /*
     * operationId: VirtualMachines_Delete
     * api-version: 2021-04-01
     * x-ms-examples: Force delete a VM
     */
    /**
     * Sample code: Force delete a VM.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void forceDeleteAVM(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachines()
            .delete("myResourceGroup", "myVM", true, Context.NONE);
    }
}
```