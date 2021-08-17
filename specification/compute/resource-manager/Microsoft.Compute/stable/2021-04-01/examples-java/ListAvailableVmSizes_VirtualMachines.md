```java
import com.azure.core.util.Context;

/** Samples for VirtualMachines ListAvailableSizes. */
public final
class ListAvailableVmSizesVirtualMachines {
    /*
     * operationId: VirtualMachines_ListAvailableSizes
     * api-version: 2021-04-01
     * x-ms-examples: Lists all available virtual machine sizes to which the specified virtual machine can be resized
     */
    /**
     * Sample code: Lists all available virtual machine sizes to which the specified virtual machine can be resized.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listsAllAvailableVirtualMachineSizesToWhichTheSpecifiedVirtualMachineCanBeResized(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachines()
            .listAvailableSizes("myResourceGroup", "myVmName", Context.NONE);
    }
}
```