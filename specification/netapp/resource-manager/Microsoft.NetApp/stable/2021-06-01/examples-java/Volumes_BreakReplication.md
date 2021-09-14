Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.netapp.models.BreakReplicationRequest;

/** Samples for Volumes BreakReplication. */
public final class Main {
    /*
     * operationId: Volumes_BreakReplication
     * api-version: 2021-06-01
     * x-ms-examples: Volumes_BreakReplication
     */
    /**
     * Sample code: Volumes_BreakReplication.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void volumesBreakReplication(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager
            .volumes()
            .breakReplication(
                "myRG",
                "account1",
                "pool1",
                "volume1",
                new BreakReplicationRequest().withForceBreakReplication(false),
                Context.NONE);
    }
}
```
