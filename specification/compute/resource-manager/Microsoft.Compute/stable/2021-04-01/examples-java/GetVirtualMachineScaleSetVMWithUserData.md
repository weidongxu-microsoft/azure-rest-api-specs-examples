```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSetVMs Get. */
public final class GetVirtualMachineScaleSetVMWithUserData {
    /*
     * operationId: VirtualMachineScaleSetVMs_Get
     * api-version: 2021-04-01
     * x-ms-examples: Get VM scale set VM with UserData
     */
    /**
     * Sample code: Get VM scale set VM with UserData.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getVMScaleSetVMWithUserData(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSetVMs()
            .getWithResponse("myResourceGroup", "{vmss-name}", "0", null, Context.NONE);
    }
}
```