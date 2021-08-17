```java
import com.azure.core.util.Context;

/** Samples for GalleryApplications Delete. */
public final class DeleteAGalleryApplication {
    /*
     * operationId: GalleryApplications_Delete
     * api-version: 2020-09-30
     * x-ms-examples: Delete a gallery Application.
     */
    /**
     * Sample code: Delete a gallery Application.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteAGalleryApplication(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryApplications()
            .delete("myResourceGroup", "myGalleryName", "myGalleryApplicationName", Context.NONE);
    }
}
```