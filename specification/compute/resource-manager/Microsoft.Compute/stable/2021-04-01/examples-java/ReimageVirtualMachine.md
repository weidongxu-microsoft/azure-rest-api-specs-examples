```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.VirtualMachineReimageParameters;

/** Samples for VirtualMachines Reimage. */
public final class ReimageVirtualMachine {
    /*
     * operationId: VirtualMachines_Reimage
     * api-version: 2021-04-01
     * x-ms-examples: Reimage a Virtual Machine.
     */
    /**
     * Sample code: Reimage a Virtual Machine.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void reimageAVirtualMachine(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachines()
            .reimage(
                "myResourceGroup", "myVMName", new VirtualMachineReimageParameters().withTempDisk(true), Context.NONE);
    }
}
```