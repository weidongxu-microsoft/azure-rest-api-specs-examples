```java
import com.azure.core.util.Context;

/** Samples for GalleryImages ListByGallery. */
public final class ListGalleryImagesInAGallery {
    /*
     * operationId: GalleryImages_ListByGallery
     * api-version: 2020-09-30
     * x-ms-examples: List gallery images in a gallery.
     */
    /**
     * Sample code: List gallery images in a gallery.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listGalleryImagesInAGallery(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryImages()
            .listByGallery("myResourceGroup", "myGalleryName", Context.NONE);
    }
}
```