Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.resourcemanager.netapp.models.ServiceLevel;

/** Samples for Volumes CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Volumes_CreateOrUpdate
     * api-version: 2021-06-01
     * x-ms-examples: Volumes_CreateOrUpdate
     */
    /**
     * Sample code: Volumes_CreateOrUpdate.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void volumesCreateOrUpdate(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager
            .volumes()
            .define("volume1")
            .withRegion("eastus")
            .withExistingCapacityPool("myRG", "account1", "pool1")
            .withCreationToken("my-unique-file-path")
            .withUsageThreshold(107374182400L)
            .withSubnetId(
                "/subscriptions/9760acf5-4638-11e7-9bdb-020073ca7778/resourceGroups/myRP/providers/Microsoft.Network/virtualNetworks/testvnet3/subnets/testsubnet3")
            .withServiceLevel(ServiceLevel.PREMIUM)
            .withThroughputMibps(128.0f)
            .withEncryptionKeySource("Microsoft.KeyVault")
            .create();
    }
}
```