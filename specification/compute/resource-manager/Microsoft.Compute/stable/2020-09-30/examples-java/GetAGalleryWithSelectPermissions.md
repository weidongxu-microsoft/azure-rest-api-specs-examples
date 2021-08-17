```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.SelectPermissions;

/** Samples for Galleries GetByResourceGroup. */
public final class GetAGalleryWithSelectPermissions {
    /*
     * operationId: Galleries_Get
     * api-version: 2020-09-30
     * x-ms-examples: Get a gallery with select permissions.
     */
    /**
     * Sample code: Get a gallery with select permissions.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAGalleryWithSelectPermissions(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleries()
            .getByResourceGroupWithResponse(
                "myResourceGroup", "myGalleryName", SelectPermissions.PERMISSIONS, Context.NONE);
    }
}
```