```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSetVMExtensions Get. */
public final class GetVirtualMachineScaleSetVMExtensions {
    /*
     * operationId: VirtualMachineScaleSetVMExtensions_Get
     * api-version: 2021-04-01
     * x-ms-examples: Get VirtualMachineScaleSet VM extension.
     */
    /**
     * Sample code: Get VirtualMachineScaleSet VM extension.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getVirtualMachineScaleSetVMExtension(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSetVMExtensions()
            .getWithResponse("myResourceGroup", "myvmScaleSet", "0", "myVMExtension", null, Context.NONE);
    }
}
```