Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for SnapshotPolicies Delete. */
public final class Main {
    /*
     * operationId: SnapshotPolicies_Delete
     * api-version: 2021-06-01
     * x-ms-examples: SnapshotPolicies_Delete
     */
    /**
     * Sample code: SnapshotPolicies_Delete.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void snapshotPoliciesDelete(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager.snapshotPolicies().delete("resourceGroup", "accountName", "snapshotPolicyName", Context.NONE);
    }
}
```
