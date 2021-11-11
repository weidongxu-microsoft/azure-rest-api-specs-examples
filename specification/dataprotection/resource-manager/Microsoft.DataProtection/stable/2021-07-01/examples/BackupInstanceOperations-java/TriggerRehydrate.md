Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-dataprotection_1.0.0-beta.1/sdk/dataprotection/azure-resourcemanager-dataprotection/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.dataprotection.models.AzureBackupRehydrationRequest;
import com.azure.resourcemanager.dataprotection.models.RehydrationPriority;

/** Samples for BackupInstances TriggerRehydrate. */
public final class Main {
    /*
     * x-ms-original-file: specification/dataprotection/resource-manager/Microsoft.DataProtection/stable/2021-07-01/examples/BackupInstanceOperations/TriggerRehydrate.json
     */
    /**
     * Sample code: Trigger Rehydrate.
     *
     * @param manager Entry point to DataProtectionManager.
     */
    public static void triggerRehydrate(com.azure.resourcemanager.dataprotection.DataProtectionManager manager) {
        manager
            .backupInstances()
            .triggerRehydrate(
                "000pikumar",
                "PratikPrivatePreviewVault1",
                "testInstance1",
                new AzureBackupRehydrationRequest()
                    .withRecoveryPointId("hardcodedRP")
                    .withRehydrationPriority(RehydrationPriority.HIGH)
                    .withRehydrationRetentionDuration("7D"),
                Context.NONE);
    }
}
```
