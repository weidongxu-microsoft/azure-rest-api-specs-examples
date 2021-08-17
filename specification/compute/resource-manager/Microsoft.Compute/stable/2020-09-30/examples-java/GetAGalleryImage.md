```java
import com.azure.core.util.Context;

/** Samples for GalleryImages Get. */
public final class GetAGalleryImage {
    /*
     * operationId: GalleryImages_Get
     * api-version: 2020-09-30
     * x-ms-examples: Get a gallery image.
     */
    /**
     * Sample code: Get a gallery image.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAGalleryImage(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryImages()
            .getWithResponse("myResourceGroup", "myGalleryName", "myGalleryImageName", Context.NONE);
    }
}
```