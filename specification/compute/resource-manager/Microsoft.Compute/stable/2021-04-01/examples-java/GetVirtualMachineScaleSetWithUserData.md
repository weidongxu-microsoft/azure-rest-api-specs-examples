```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSets GetByResourceGroup. */
public final class GetVirtualMachineScaleSetWithUserData {
    /*
     * operationId: VirtualMachineScaleSets_Get
     * api-version: 2021-04-01
     * x-ms-examples: Get a virtual machine scale set with UserData
     */
    /**
     * Sample code: Get a virtual machine scale set with UserData.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAVirtualMachineScaleSetWithUserData(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSets()
            .getByResourceGroupWithResponse("myResourceGroup", "myVirtualMachineScaleSet", null, Context.NONE);
    }
}
```