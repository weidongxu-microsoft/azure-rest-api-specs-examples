Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java

/** Samples for Backups Create. */
public final class Main {
    /*
     * operationId: Backups_Create
     * api-version: 2021-06-01
     * x-ms-examples: Backups_Create
     */
    /**
     * Sample code: Backups_Create.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void backupsCreate(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager
            .backups()
            .define("backup1")
            .withRegion("eastus")
            .withExistingVolume("myRG", "account1", "pool1", "volume1")
            .withLabel("myLabel")
            .create();
    }
}
```
