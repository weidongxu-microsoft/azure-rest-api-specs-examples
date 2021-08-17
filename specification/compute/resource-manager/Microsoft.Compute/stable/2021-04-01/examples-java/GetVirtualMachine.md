```java
import com.azure.core.util.Context;

/** Samples for VirtualMachines GetByResourceGroup. */
public final class GetVirtualMachine {
    /*
     * operationId: VirtualMachines_Get
     * api-version: 2021-04-01
     * x-ms-examples: Get a Virtual Machine.
     */
    /**
     * Sample code: Get a Virtual Machine.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAVirtualMachine(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachines()
            .getByResourceGroupWithResponse("myResourceGroup", "myVM", null, Context.NONE);
    }
}
```