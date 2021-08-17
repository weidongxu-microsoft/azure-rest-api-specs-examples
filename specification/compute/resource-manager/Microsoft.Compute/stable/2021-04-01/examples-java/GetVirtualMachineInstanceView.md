```java
import com.azure.core.util.Context;

/** Samples for VirtualMachines InstanceView. */
public final class GetVirtualMachineInstanceView {
    /*
     * operationId: VirtualMachines_InstanceView
     * api-version: 2021-04-01
     * x-ms-examples: Get Virtual Machine Instance View.
     */
    /**
     * Sample code: Get Virtual Machine Instance View.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getVirtualMachineInstanceView(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachines()
            .instanceViewWithResponse("myResourceGroup", "myVM", Context.NONE);
    }
}
```