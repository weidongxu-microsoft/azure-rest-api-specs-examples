Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-dataprotection_1.0.0-beta.1/sdk/dataprotection/azure-resourcemanager-dataprotection/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.resourcemanager.dataprotection.models.BackupVault;
import com.azure.resourcemanager.dataprotection.models.DppIdentityDetails;
import com.azure.resourcemanager.dataprotection.models.StorageSetting;
import com.azure.resourcemanager.dataprotection.models.StorageSettingStoreTypes;
import com.azure.resourcemanager.dataprotection.models.StorageSettingTypes;
import java.util.Arrays;
import java.util.HashMap;
import java.util.Map;

/** Samples for BackupVaults CreateOrUpdate. */
public final class Main {
    /*
     * x-ms-original-file: specification/dataprotection/resource-manager/Microsoft.DataProtection/stable/2021-07-01/examples/VaultCRUD/PutBackupVaultWithMSI.json
     */
    /**
     * Sample code: Create BackupVault With MSI.
     *
     * @param manager Entry point to DataProtectionManager.
     */
    public static void createBackupVaultWithMSI(
        com.azure.resourcemanager.dataprotection.DataProtectionManager manager) {
        manager
            .backupVaults()
            .define("swaggerExample")
            .withRegion("WestUS")
            .withExistingResourceGroup("SampleResourceGroup")
            .withProperties(
                new BackupVault()
                    .withStorageSettings(
                        Arrays
                            .asList(
                                new StorageSetting()
                                    .withDatastoreType(StorageSettingStoreTypes.VAULT_STORE)
                                    .withType(StorageSettingTypes.LOCALLY_REDUNDANT))))
            .withTags(mapOf("key1", "val1"))
            .withIdentity(new DppIdentityDetails().withType("systemAssigned"))
            .create();
    }

    @SuppressWarnings("unchecked")
    private static <T> Map<String, T> mapOf(Object... inputs) {
        Map<String, T> map = new HashMap<>();
        for (int i = 0; i < inputs.length; i += 2) {
            String key = (String) inputs[i];
            T value = (T) inputs[i + 1];
            map.put(key, value);
        }
        return map;
    }
}
```
