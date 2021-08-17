```java
import com.azure.core.util.Context;

/** Samples for Snapshots List. */
public final class ListSnapshotsInASubscription {
    /*
     * operationId: Snapshots_List
     * api-version: 2020-12-01
     * x-ms-examples: List all snapshots in a subscription.
     */
    /**
     * Sample code: List all snapshots in a subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listAllSnapshotsInASubscription(com.azure.resourcemanager.AzureResourceManager azure) {
        azure.virtualMachines().manager().serviceClient().getSnapshots().list(Context.NONE);
    }
}
```