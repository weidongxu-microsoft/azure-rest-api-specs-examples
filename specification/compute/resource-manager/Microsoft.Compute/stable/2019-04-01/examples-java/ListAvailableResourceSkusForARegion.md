```java
import com.azure.core.util.Context;

/** Samples for ResourceSkus List. */
public final class ListAvailableResourceSkusForARegion {
    /*
     * operationId: ResourceSkus_List
     * api-version: 2019-04-01
     * x-ms-examples: Lists all available Resource SKUs for the specified region
     */
    /**
     * Sample code: Lists all available Resource SKUs for the specified region.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listsAllAvailableResourceSKUsForTheSpecifiedRegion(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure.virtualMachines().manager().serviceClient().getResourceSkus().list("location eq 'westus'", Context.NONE);
    }
}
```