Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java
/** Samples for Snapshots Create. */
public final class Main {
    /*
     * operationId: Snapshots_Create
     * api-version: 2021-06-01
     * x-ms-examples: Snapshots_Create
     */
    /**
     * Sample code: Snapshots_Create.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void snapshotsCreate(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager
            .snapshots()
            .define("snapshot1")
            .withRegion("eastus")
            .withExistingVolume("myRG", "account1", "pool1", "volume1")
            .create();
    }
}
```
