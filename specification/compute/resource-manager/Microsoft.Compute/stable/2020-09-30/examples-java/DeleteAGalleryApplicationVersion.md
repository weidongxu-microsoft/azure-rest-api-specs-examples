```java
import com.azure.core.util.Context;

/** Samples for GalleryApplicationVersions Delete. */
public final class DeleteAGalleryApplicationVersion {
    /*
     * operationId: GalleryApplicationVersions_Delete
     * api-version: 2020-09-30
     * x-ms-examples: Delete a gallery Application Version.
     */
    /**
     * Sample code: Delete a gallery Application Version.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteAGalleryApplicationVersion(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryApplicationVersions()
            .delete("myResourceGroup", "myGalleryName", "myGalleryApplicationName", "1.0.0", Context.NONE);
    }
}
```