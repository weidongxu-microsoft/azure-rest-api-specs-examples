Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Snapshots Delete. */
public final class Main {
    /*
     * operationId: Snapshots_Delete
     * api-version: 2021-06-01
     * x-ms-examples: Snapshots_Delete
     */
    /**
     * Sample code: Snapshots_Delete.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void snapshotsDelete(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager.snapshots().delete("myRG", "account1", "pool1", "volume1", "snapshot1", Context.NONE);
    }
}
```
