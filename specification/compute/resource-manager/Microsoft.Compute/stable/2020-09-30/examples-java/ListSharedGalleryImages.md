```java
import com.azure.core.util.Context;

/** Samples for SharedGalleryImages List. */
public final class ListSharedGalleryImages {
    /*
     * operationId: SharedGalleryImages_List
     * api-version: 2020-09-30
     * x-ms-examples: Get a gallery.
     */
    /**
     * Sample code: Get a gallery.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAGallery(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getSharedGalleryImages()
            .list("myLocation", "galleryUniqueName", null, Context.NONE);
    }
}
```