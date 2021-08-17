```java
import com.azure.core.util.Context;

/** Samples for DiskEncryptionSets List. */
public final class ListDiskEncryptionSetsInASubscription {
    /*
     * operationId: DiskEncryptionSets_List
     * api-version: 2020-12-01
     * x-ms-examples: List all disk encryption sets in a subscription.
     */
    /**
     * Sample code: List all disk encryption sets in a subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listAllDiskEncryptionSetsInASubscription(com.azure.resourcemanager.AzureResourceManager azure) {
        azure.virtualMachines().manager().serviceClient().getDiskEncryptionSets().list(Context.NONE);
    }
}
```