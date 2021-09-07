Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Snapshots Get. */
public final class Main {
    /*
     * operationId: Snapshots_Get
     * api-version: 2021-06-01
     * x-ms-examples: Snapshots_Get
     */
    /**
     * Sample code: Snapshots_Get.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void snapshotsGet(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager.snapshots().getWithResponse("myRG", "account1", "pool1", "volume1", "snapshot1", Context.NONE);
    }
}
```