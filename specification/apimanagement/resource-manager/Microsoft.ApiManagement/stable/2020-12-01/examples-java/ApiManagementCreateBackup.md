Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.ApiManagementServiceBackupRestoreParameters;

/** Samples for ApiManagementService Backup. */
public final class Main {
    /*
     * operationId: ApiManagementService_Backup
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateBackup
     */
    /**
     * Sample code: ApiManagementCreateBackup.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateBackup(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apiManagementServices()
            .backup(
                "rg1",
                "apimService1",
                new ApiManagementServiceBackupRestoreParameters()
                    .withStorageAccount("teststorageaccount")
                    .withAccessKey("**************************************************")
                    .withContainerName("backupContainer")
                    .withBackupName("apimService1backup_2017_03_19"),
                Context.NONE);
    }
}
```
