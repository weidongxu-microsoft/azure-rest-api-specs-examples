Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for BackupPolicies List. */
public final class Main {
    /*
     * operationId: BackupPolicies_List
     * api-version: 2021-06-01
     * x-ms-examples: Backups_List
     */
    /**
     * Sample code: Backups_List.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void backupsList(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager.backupPolicies().list("myRG", "account1", Context.NONE);
    }
}
```