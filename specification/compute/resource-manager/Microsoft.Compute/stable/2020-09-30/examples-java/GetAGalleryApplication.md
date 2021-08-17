```java
import com.azure.core.util.Context;

/** Samples for GalleryApplications Get. */
public final class GetAGalleryApplication {
    /*
     * operationId: GalleryApplications_Get
     * api-version: 2020-09-30
     * x-ms-examples: Get a gallery Application.
     */
    /**
     * Sample code: Get a gallery Application.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAGalleryApplication(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryApplications()
            .getWithResponse("myResourceGroup", "myGalleryName", "myGalleryApplicationName", Context.NONE);
    }
}
```