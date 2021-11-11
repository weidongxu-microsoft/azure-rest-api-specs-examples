Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-dataprotection_1.0.0-beta.1/sdk/dataprotection/azure-resourcemanager-dataprotection/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.dataprotection.models.AzureBackupFindRestorableTimeRangesRequest;
import com.azure.resourcemanager.dataprotection.models.RestoreSourceDataStoreType;

/** Samples for RestorableTimeRanges Find. */
public final class Main {
    /*
     * x-ms-original-file: specification/dataprotection/resource-manager/Microsoft.DataProtection/stable/2021-07-01/examples/BackupInstanceOperations/FindRestorableTimeRanges.json
     */
    /**
     * Sample code: Find Restorable Time Ranges.
     *
     * @param manager Entry point to DataProtectionManager.
     */
    public static void findRestorableTimeRanges(
        com.azure.resourcemanager.dataprotection.DataProtectionManager manager) {
        manager
            .restorableTimeRanges()
            .findWithResponse(
                "ZBlobBackupVaultBVTD3",
                "Blob-Backup",
                "zblobbackuptestsa58",
                new AzureBackupFindRestorableTimeRangesRequest()
                    .withSourceDataStoreType(RestoreSourceDataStoreType.OPERATIONAL_STORE)
                    .withStartTime("2020-10-17T23:28:17.6829685Z")
                    .withEndTime("2021-02-24T00:35:17.6829685Z"),
                Context.NONE);
    }
}
```
