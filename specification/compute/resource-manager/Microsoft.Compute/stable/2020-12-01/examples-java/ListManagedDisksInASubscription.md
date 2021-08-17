```java
import com.azure.core.util.Context;

/** Samples for Disks List. */
public final class ListManagedDisksInASubscription {
    /*
     * operationId: Disks_List
     * api-version: 2020-12-01
     * x-ms-examples: List all managed disks in a subscription.
     */
    /**
     * Sample code: List all managed disks in a subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listAllManagedDisksInASubscription(com.azure.resourcemanager.AzureResourceManager azure) {
        azure.virtualMachines().manager().serviceClient().getDisks().list(Context.NONE);
    }
}
```