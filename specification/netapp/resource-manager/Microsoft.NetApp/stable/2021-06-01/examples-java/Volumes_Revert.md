Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.netapp.models.VolumeRevert;

/** Samples for Volumes Revert. */
public final class Main {
    /*
     * operationId: Volumes_Revert
     * api-version: 2021-06-01
     * x-ms-examples: Volumes_Revert
     */
    /**
     * Sample code: Volumes_Revert.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void volumesRevert(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager
            .volumes()
            .revert(
                "myRG",
                "account1",
                "pool1",
                "volume1",
                new VolumeRevert()
                    .withSnapshotId(
                        "/subscriptions/D633CC2E-722B-4AE1-B636-BBD9E4C60ED9/resourceGroups/myRG/providers/Microsoft.NetApp/netAppAccounts/account1/capacityPools/pool1/volumes/volume1/snapshots/snapshot1"),
                Context.NONE);
    }
}
```
