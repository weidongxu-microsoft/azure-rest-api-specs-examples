```java
import com.azure.core.util.Context;

/** Samples for GalleryImages Delete. */
public final class DeleteAGalleryImage {
    /*
     * operationId: GalleryImages_Delete
     * api-version: 2020-09-30
     * x-ms-examples: Delete a gallery image.
     */
    /**
     * Sample code: Delete a gallery image.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteAGalleryImage(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryImages()
            .delete("myResourceGroup", "myGalleryName", "myGalleryImageName", Context.NONE);
    }
}
```