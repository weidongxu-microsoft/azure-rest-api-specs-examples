```java
import com.azure.core.util.Context;

/** Samples for Galleries ListByResourceGroup. */
public final class ListGalleriesInAResourceGroup {
    /*
     * operationId: Galleries_ListByResourceGroup
     * api-version: 2020-09-30
     * x-ms-examples: List galleries in a resource group.
     */
    /**
     * Sample code: List galleries in a resource group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listGalleriesInAResourceGroup(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleries()
            .listByResourceGroup("myResourceGroup", Context.NONE);
    }
}
```