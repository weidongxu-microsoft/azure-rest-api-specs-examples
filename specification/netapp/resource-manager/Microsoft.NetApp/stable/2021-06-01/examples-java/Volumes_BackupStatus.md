Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Backups GetStatus. */
public final class Main {
    /*
     * operationId: Backups_GetStatus
     * api-version: 2021-06-01
     * x-ms-examples: Volumes_BackupStatus
     */
    /**
     * Sample code: Volumes_BackupStatus.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void volumesBackupStatus(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager.backups().getStatusWithResponse("myRG", "account1", "pool1", "volume1", Context.NONE);
    }
}
```
