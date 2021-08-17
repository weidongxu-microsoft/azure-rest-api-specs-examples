```java
import com.azure.core.util.Context;

/** Samples for CloudServices List. */
public final class ListCloudServicesInSubscription {
    /*
     * operationId: CloudServices_ListAll
     * api-version: 2021-03-01
     * x-ms-examples: List Cloud Services in a Subscription
     */
    /**
     * Sample code: List Cloud Services in a Subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listCloudServicesInASubscription(com.azure.resourcemanager.AzureResourceManager azure) {
        azure.virtualMachines().manager().serviceClient().getCloudServices().list(Context.NONE);
    }
}
```