Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.netapp.models.PoolChangeRequest;

/** Samples for Volumes PoolChange. */
public final class Main {
    /*
     * operationId: Volumes_PoolChange
     * api-version: 2021-06-01
     * x-ms-examples: Volumes_AuthorizeReplication
     */
    /**
     * Sample code: Volumes_AuthorizeReplication.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void volumesAuthorizeReplication(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager
            .volumes()
            .poolChange(
                "myRG",
                "account1",
                "pool1",
                "volume1",
                new PoolChangeRequest()
                    .withNewPoolResourceId(
                        "/subscriptions/D633CC2E-722B-4AE1-B636-BBD9E4C60ED9/resourceGroups/myRG/providers/Microsoft.NetApp/netAppAccounts/account1/capacityPools/pool1"),
                Context.NONE);
    }
}
```
