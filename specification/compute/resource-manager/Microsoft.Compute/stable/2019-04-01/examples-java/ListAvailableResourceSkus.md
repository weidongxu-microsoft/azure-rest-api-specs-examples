```java
import com.azure.core.util.Context;

/** Samples for ResourceSkus List. */
public final class ListAvailableResourceSkus {
    /*
     * operationId: ResourceSkus_List
     * api-version: 2019-04-01
     * x-ms-examples: Lists all available Resource SKUs
     */
    /**
     * Sample code: Lists all available Resource SKUs.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listsAllAvailableResourceSKUs(com.azure.resourcemanager.AzureResourceManager azure) {
        azure.virtualMachines().manager().serviceClient().getResourceSkus().list(null, Context.NONE);
    }
}
```