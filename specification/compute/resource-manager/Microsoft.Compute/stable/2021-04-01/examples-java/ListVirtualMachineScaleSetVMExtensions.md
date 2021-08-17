```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSetVMExtensions List. */
public final class ListVirtualMachineScaleSetVMExtensions {
    /*
     * operationId: VirtualMachineScaleSetVMExtensions_List
     * api-version: 2021-04-01
     * x-ms-examples: List extensions in Vmss instance.
     */
    /**
     * Sample code: List extensions in Vmss instance.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listExtensionsInVmssInstance(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSetVMExtensions()
            .listWithResponse("myResourceGroup", "myvmScaleSet", "0", null, Context.NONE);
    }
}
```