Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java

/** Samples for BackupPolicies Create. */
public final class Main {
    /*
     * operationId: BackupPolicies_Create
     * api-version: 2021-06-01
     * x-ms-examples: BackupPolicies_Create
     */
    /**
     * Sample code: BackupPolicies_Create.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void backupPoliciesCreate(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager
            .backupPolicies()
            .define("backupPolicyName")
            .withRegion("westus")
            .withExistingNetAppAccount("myRG", "account1")
            .withDailyBackupsToKeep(10)
            .withWeeklyBackupsToKeep(10)
            .withMonthlyBackupsToKeep(10)
            .withEnabled(true)
            .create();
    }
}
```
