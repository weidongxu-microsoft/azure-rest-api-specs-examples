```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.DiskEncryptionSetInner;
import com.azure.resourcemanager.compute.models.DiskEncryptionSetIdentityType;
import com.azure.resourcemanager.compute.models.DiskEncryptionSetType;
import com.azure.resourcemanager.compute.models.EncryptionSetIdentity;
import com.azure.resourcemanager.compute.models.KeyForDiskEncryptionSet;

/** Samples for DiskEncryptionSets CreateOrUpdate. */
public final
class CreateADiskEncryptionSetWithKeyVaultFromADifferentSubscription {
    /*
     * operationId: DiskEncryptionSets_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: Create a disk encryption set with key vault from a different subscription.
     */
    /**
     * Sample code: Create a disk encryption set with key vault from a different subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createADiskEncryptionSetWithKeyVaultFromADifferentSubscription(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDiskEncryptionSets()
            .createOrUpdate(
                "myResourceGroup",
                "myDiskEncryptionSet",
                new DiskEncryptionSetInner()
                    .withLocation("West US")
                    .withIdentity(new EncryptionSetIdentity().withType(DiskEncryptionSetIdentityType.SYSTEM_ASSIGNED))
                    .withEncryptionType(DiskEncryptionSetType.ENCRYPTION_AT_REST_WITH_CUSTOMER_KEY)
                    .withActiveKey(
                        new KeyForDiskEncryptionSet()
                            .withKeyUrl("https://myvaultdifferentsub.vault-int.azure-int.net/keys/{key}")),
                Context.NONE);
    }
}
```