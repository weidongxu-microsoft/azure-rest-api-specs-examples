```java
import com.azure.core.util.Context;

/** Samples for Galleries List. */
public final class ListGalleriesInASubscription {
    /*
     * operationId: Galleries_List
     * api-version: 2020-09-30
     * x-ms-examples: List galleries in a subscription.
     */
    /**
     * Sample code: List galleries in a subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listGalleriesInASubscription(com.azure.resourcemanager.AzureResourceManager azure) {
        azure.virtualMachines().manager().serviceClient().getGalleries().list(Context.NONE);
    }
}
```