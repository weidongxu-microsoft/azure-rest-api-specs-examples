Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-dataprotection_1.0.0-beta.1/sdk/dataprotection/azure-resourcemanager-dataprotection/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.dataprotection.models.AdHocBackupRuleOptions;
import com.azure.resourcemanager.dataprotection.models.AdhocBackupTriggerOption;
import com.azure.resourcemanager.dataprotection.models.TriggerBackupRequest;

/** Samples for BackupInstances AdhocBackup. */
public final class Main {
    /*
     * x-ms-original-file: specification/dataprotection/resource-manager/Microsoft.DataProtection/stable/2021-07-01/examples/BackupInstanceOperations/TriggerBackup.json
     */
    /**
     * Sample code: Trigger Adhoc Backup.
     *
     * @param manager Entry point to DataProtectionManager.
     */
    public static void triggerAdhocBackup(com.azure.resourcemanager.dataprotection.DataProtectionManager manager) {
        manager
            .backupInstances()
            .adhocBackup(
                "PratikPrivatePreviewVault1",
                "000pikumar",
                "testInstance1",
                new TriggerBackupRequest()
                    .withBackupRuleOptions(
                        new AdHocBackupRuleOptions()
                            .withRuleName("BackupWeekly")
                            .withTriggerOption(new AdhocBackupTriggerOption().withRetentionTagOverride("yearly"))),
                Context.NONE);
    }
}
```
