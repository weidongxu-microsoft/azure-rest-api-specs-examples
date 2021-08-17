```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSets Delete. */
public final class ForceDeleteVirtualMachineScaleSets {
    /*
     * operationId: VirtualMachineScaleSets_Delete
     * api-version: 2021-04-01
     * x-ms-examples: Force Delete a VM scale set.
     */
    /**
     * Sample code: Force Delete a VM scale set.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void forceDeleteAVMScaleSet(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSets()
            .delete("myResourceGroup", "myvmScaleSet", true, Context.NONE);
    }
}
```