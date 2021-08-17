```java
import com.azure.core.util.Context;

/** Samples for AvailabilitySets List. */
public final class ListAvailabilitySetsInASubscription {
    /*
     * operationId: AvailabilitySets_ListBySubscription
     * api-version: 2021-04-01
     * x-ms-examples: List availability sets in a subscription.
     */
    /**
     * Sample code: List availability sets in a subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listAvailabilitySetsInASubscription(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getAvailabilitySets()
            .list("virtualMachines\\$ref", Context.NONE);
    }
}
```