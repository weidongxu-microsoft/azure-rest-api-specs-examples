Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Volumes List. */
public final class Main {
    /*
     * operationId: Volumes_List
     * api-version: 2021-06-01
     * x-ms-examples: Volumes_List
     */
    /**
     * Sample code: Volumes_List.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void volumesList(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager.volumes().list("myRG", "account1", "pool1", Context.NONE);
    }
}
```
