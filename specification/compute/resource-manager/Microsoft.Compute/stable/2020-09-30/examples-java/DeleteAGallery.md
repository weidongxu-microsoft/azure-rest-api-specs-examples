```java
import com.azure.core.util.Context;

/** Samples for Galleries Delete. */
public final class DeleteAGallery {
    /*
     * operationId: Galleries_Delete
     * api-version: 2020-09-30
     * x-ms-examples: Delete a gallery.
     */
    /**
     * Sample code: Delete a gallery.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteAGallery(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleries()
            .delete("myResourceGroup", "myGalleryName", Context.NONE);
    }
}
```