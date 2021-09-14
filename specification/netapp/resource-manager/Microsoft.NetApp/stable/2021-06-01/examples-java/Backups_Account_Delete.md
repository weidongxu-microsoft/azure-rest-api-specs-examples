Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for AccountBackups Delete. */
public final class Main {
    /*
     * operationId: AccountBackups_Delete
     * api-version: 2021-06-01
     * x-ms-examples: AccountBackups_Delete
     */
    /**
     * Sample code: AccountBackups_Delete.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void accountBackupsDelete(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager.accountBackups().delete("resourceGroup", "accountName", "backupName", Context.NONE);
    }
}
```
