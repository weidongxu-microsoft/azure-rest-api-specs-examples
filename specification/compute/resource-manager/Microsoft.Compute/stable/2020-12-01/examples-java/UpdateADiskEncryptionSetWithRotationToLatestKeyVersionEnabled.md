```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.DiskEncryptionSetIdentityType;
import com.azure.resourcemanager.compute.models.DiskEncryptionSetType;
import com.azure.resourcemanager.compute.models.DiskEncryptionSetUpdate;
import com.azure.resourcemanager.compute.models.EncryptionSetIdentity;
import com.azure.resourcemanager.compute.models.KeyForDiskEncryptionSet;

/** Samples for DiskEncryptionSets Update. */
public final
class UpdateADiskEncryptionSetWithRotationToLatestKeyVersionEnabled {
    /*
     * operationId: DiskEncryptionSets_Update
     * api-version: 2020-12-01
     * x-ms-examples: Update a disk encryption set with rotationToLatestKeyVersionEnabled set to true - Succeeded
     */
    /**
     * Sample code: Update a disk encryption set with rotationToLatestKeyVersionEnabled set to true - Succeeded.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void updateADiskEncryptionSetWithRotationToLatestKeyVersionEnabledSetToTrueSucceeded(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskEncryptionSets()
            .update(
                "myResourceGroup",
                "myDiskEncryptionSet",
                new DiskEncryptionSetUpdate()
                    .withIdentity(new EncryptionSetIdentity().withType(DiskEncryptionSetIdentityType.SYSTEM_ASSIGNED))
                    .withEncryptionType(DiskEncryptionSetType.ENCRYPTION_AT_REST_WITH_CUSTOMER_KEY)
                    .withActiveKey(
                        new KeyForDiskEncryptionSet()
                            .withKeyUrl("https://myvaultdifferentsub.vault-int.azure-int.net/keys/keyName/keyVersion1"))
                    .withRotationToLatestKeyVersionEnabled(true),
                Context.NONE);
    }
}
```