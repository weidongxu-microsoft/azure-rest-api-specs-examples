Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager_2.10.0/sdk/resourcemanager/azure-resourcemanager/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.DiskEncryptionSetIdentityType;
import com.azure.resourcemanager.compute.models.DiskEncryptionSetType;
import com.azure.resourcemanager.compute.models.DiskEncryptionSetUpdate;
import com.azure.resourcemanager.compute.models.EncryptionSetIdentity;
import com.azure.resourcemanager.compute.models.KeyForDiskEncryptionSet;
import java.util.HashMap;
import java.util.Map;

/** Samples for DiskEncryptionSets Update. */
public final class Main {
    /*
     * x-ms-original-file: specification/compute/resource-manager/Microsoft.Compute/stable/2021-04-01/examples/UpdateADiskEncryptionSetWithRotationToLatestKeyVersionEnabledInProgress.json
     */
    /**
     * Sample code: Update a disk encryption set with rotationToLatestKeyVersionEnabled set to true - Updating.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void updateADiskEncryptionSetWithRotationToLatestKeyVersionEnabledSetToTrueUpdating(
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
