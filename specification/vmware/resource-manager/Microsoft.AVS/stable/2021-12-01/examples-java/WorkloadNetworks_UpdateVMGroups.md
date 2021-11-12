Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-avs_1.0.0-beta.3/sdk/avs/azure-resourcemanager-avs/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.avs.models.WorkloadNetworkVMGroup;
import java.util.Arrays;

/** Samples for WorkloadNetworks UpdateVMGroup. */
public final class Main {
    /*
     * x-ms-original-file: specification/vmware/resource-manager/Microsoft.AVS/stable/2021-12-01/examples/WorkloadNetworks_UpdateVMGroups.json
     */
    /**
     * Sample code: WorkloadNetworks_UpdateVMGroup.
     *
     * @param manager Entry point to AvsManager.
     */
    public static void workloadNetworksUpdateVMGroup(com.azure.resourcemanager.avs.AvsManager manager) {
        WorkloadNetworkVMGroup resource =
            manager.workloadNetworks().getVMGroupWithResponse("group1", "cloud1", "vmGroup1", Context.NONE).getValue();
        resource.update().withMembers(Arrays.asList("564d43da-fefc-2a3b-1d92-42855622fa50")).withRevision(1L).apply();
    }
}
```