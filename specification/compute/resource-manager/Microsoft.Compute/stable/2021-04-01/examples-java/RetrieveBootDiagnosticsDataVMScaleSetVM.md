```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSetVMs RetrieveBootDiagnosticsData. */
public final
class RetrieveBootDiagnosticsDataVMScaleSetVM {
    /*
     * operationId: VirtualMachineScaleSetVMs_RetrieveBootDiagnosticsData
     * api-version: 2021-04-01
     * x-ms-examples: RetrieveBootDiagnosticsData of a virtual machine.
     */
    /**
     * Sample code: RetrieveBootDiagnosticsData of a virtual machine.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void retrieveBootDiagnosticsDataOfAVirtualMachine(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSetVMs()
            .retrieveBootDiagnosticsDataWithResponse("ResourceGroup", "myvmScaleSet", "0", 60, Context.NONE);
    }
}
```