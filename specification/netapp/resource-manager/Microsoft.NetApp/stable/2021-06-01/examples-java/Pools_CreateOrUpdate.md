Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.resourcemanager.netapp.models.QosType;
import com.azure.resourcemanager.netapp.models.ServiceLevel;

/** Samples for Pools CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Pools_CreateOrUpdate
     * api-version: 2021-06-01
     * x-ms-examples: Pools_CreateOrUpdate
     */
    /**
     * Sample code: Pools_CreateOrUpdate.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void poolsCreateOrUpdate(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager
            .pools()
            .define("pool1")
            .withRegion("eastus")
            .withExistingNetAppAccount("myRG", "account1")
            .withSize(4398046511104L)
            .withServiceLevel(ServiceLevel.PREMIUM)
            .withQosType(QosType.AUTO)
            .create();
    }
}
```
