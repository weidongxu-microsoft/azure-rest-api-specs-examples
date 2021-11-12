Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-dataprotection_1.0.0-beta.1/sdk/dataprotection/azure-resourcemanager-dataprotection/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.dataprotection.models.CheckNameAvailabilityRequest;

/** Samples for BackupVaults CheckNameAvailability. */
public final class Main {
    /*
     * x-ms-original-file: specification/dataprotection/resource-manager/Microsoft.DataProtection/stable/2021-07-01/examples/VaultCRUD/CheckBackupVaultsNameAvailability.json
     */
    /**
     * Sample code: Check BackupVaults name availability.
     *
     * @param manager Entry point to DataProtectionManager.
     */
    public static void checkBackupVaultsNameAvailability(
        com.azure.resourcemanager.dataprotection.DataProtectionManager manager) {
        manager
            .backupVaults()
            .checkNameAvailabilityWithResponse(
                "SampleResourceGroup",
                "westus",
                new CheckNameAvailabilityRequest()
                    .withName("swaggerExample")
                    .withType("Microsoft.DataProtection/BackupVaults"),
                Context.NONE);
    }
}
```
