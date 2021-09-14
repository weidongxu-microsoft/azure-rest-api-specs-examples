Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Pools Get. */
public final class Main {
    /*
     * operationId: Pools_Get
     * api-version: 2021-06-01
     * x-ms-examples: Pools_Get
     */
    /**
     * Sample code: Pools_Get.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void poolsGet(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager.pools().getWithResponse("myRG", "account1", "pool1", Context.NONE);
    }
}
```
