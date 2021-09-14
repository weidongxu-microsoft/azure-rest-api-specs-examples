Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for SnapshotPolicies ListVolumes. */
public final class Main {
    /*
     * operationId: SnapshotPolicies_ListVolumes
     * api-version: 2021-06-01
     * x-ms-examples: SnapshotPolicies_ListVolumes
     */
    /**
     * Sample code: SnapshotPolicies_ListVolumes.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void snapshotPoliciesListVolumes(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager.snapshotPolicies().listVolumesWithResponse("myRG", "account1", "snapshotPolicyName", Context.NONE);
    }
}
```
