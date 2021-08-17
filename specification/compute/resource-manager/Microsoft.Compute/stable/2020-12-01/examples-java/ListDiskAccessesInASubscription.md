```java
import com.azure.core.util.Context;

/** Samples for DiskAccesses List. */
public final class ListDiskAccessesInASubscription {
    /*
     * operationId: DiskAccesses_List
     * api-version: 2020-12-01
     * x-ms-examples: List all disk access resources in a subscription.
     */
    /**
     * Sample code: List all disk access resources in a subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listAllDiskAccessResourcesInASubscription(com.azure.resourcemanager.AzureResourceManager azure) {
        azure.virtualMachines().manager().serviceClient().getDiskAccesses().list(Context.NONE);
    }
}
```