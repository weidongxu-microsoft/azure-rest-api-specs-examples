```java
import com.azure.core.util.Context;

/** Samples for RestorePointCollections List. */
public final class GetRestorePointCollectionsInASubscription {
    /*
     * operationId: RestorePointCollections_ListAll
     * api-version: 2021-04-01
     * x-ms-examples: Gets the list of restore point collections in a subscription
     */
    /**
     * Sample code: Gets the list of restore point collections in a subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getsTheListOfRestorePointCollectionsInASubscription(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure.virtualMachines().manager().serviceClient().getRestorePointCollections().list(Context.NONE);
    }
}
```