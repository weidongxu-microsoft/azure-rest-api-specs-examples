```java
import com.azure.core.util.Context;

/** Samples for GalleryApplications ListByGallery. */
public final class ListGalleryApplicationsInAGallery {
    /*
     * operationId: GalleryApplications_ListByGallery
     * api-version: 2020-09-30
     * x-ms-examples: List gallery Applications in a gallery.
     */
    /**
     * Sample code: List gallery Applications in a gallery.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listGalleryApplicationsInAGallery(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryApplications()
            .listByGallery("myResourceGroup", "myGalleryName", Context.NONE);
    }
}
```