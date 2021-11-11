Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-dataprotection_1.0.0-beta.1/sdk/dataprotection/azure-resourcemanager-dataprotection/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.dataprotection.models.AzureBackupRecoveryPointBasedRestoreRequest;
import com.azure.resourcemanager.dataprotection.models.Datasource;
import com.azure.resourcemanager.dataprotection.models.DatasourceSet;
import com.azure.resourcemanager.dataprotection.models.RecoveryOption;
import com.azure.resourcemanager.dataprotection.models.RestoreTargetInfo;
import com.azure.resourcemanager.dataprotection.models.SecretStoreBasedAuthCredentials;
import com.azure.resourcemanager.dataprotection.models.SecretStoreResource;
import com.azure.resourcemanager.dataprotection.models.SecretStoreType;
import com.azure.resourcemanager.dataprotection.models.SourceDataStoreType;

/** Samples for BackupInstances TriggerRestore. */
public final class Main {
    /*
     * x-ms-original-file: specification/dataprotection/resource-manager/Microsoft.DataProtection/stable/2021-07-01/examples/BackupInstanceOperations/TriggerRestore.json
     */
    /**
     * Sample code: Trigger Restore.
     *
     * @param manager Entry point to DataProtectionManager.
     */
    public static void triggerRestore(com.azure.resourcemanager.dataprotection.DataProtectionManager manager) {
        manager
            .backupInstances()
            .triggerRestore(
                "PratikPrivatePreviewVault1",
                "000pikumar",
                "testInstance1",
                new AzureBackupRecoveryPointBasedRestoreRequest()
                    .withRestoreTargetInfo(
                        new RestoreTargetInfo()
                            .withRecoveryOption(RecoveryOption.FAIL_IF_EXISTS)
                            .withRestoreLocation("southeastasia")
                            .withDatasourceInfo(
                                new Datasource()
                                    .withDatasourceType("OssDB")
                                    .withObjectType("Datasource")
                                    .withResourceId(
                                        "/subscriptions/f75d8d8b-6735-4697-82e1-1a7a3ff0d5d4/resourceGroups/viveksipgtest/providers/Microsoft.DBforPostgreSQL/servers/viveksipgtest/databases/testdb")
                                    .withResourceLocation("")
                                    .withResourceName("testdb")
                                    .withResourceType("Microsoft.DBforPostgreSQL/servers/databases")
                                    .withResourceUri(""))
                            .withDatasourceSetInfo(
                                new DatasourceSet()
                                    .withDatasourceType("OssDB")
                                    .withObjectType("DatasourceSet")
                                    .withResourceId(
                                        "/subscriptions/f75d8d8b-6735-4697-82e1-1a7a3ff0d5d4/resourceGroups/viveksipgtest/providers/Microsoft.DBforPostgreSQL/servers/viveksipgtest")
                                    .withResourceLocation("")
                                    .withResourceName("viveksipgtest")
                                    .withResourceType("Microsoft.DBforPostgreSQL/servers")
                                    .withResourceUri(""))
                            .withDatasourceAuthCredentials(
                                new SecretStoreBasedAuthCredentials()
                                    .withSecretStoreResource(
                                        new SecretStoreResource()
                                            .withUri("https://samplevault.vault.azure.net/secrets/credentials")
                                            .withSecretStoreType(SecretStoreType.AZURE_KEY_VAULT))))
                    .withSourceDataStoreType(SourceDataStoreType.VAULT_STORE)
                    .withRecoveryPointId("hardcodedRP"),
                Context.NONE);
    }
}
```
