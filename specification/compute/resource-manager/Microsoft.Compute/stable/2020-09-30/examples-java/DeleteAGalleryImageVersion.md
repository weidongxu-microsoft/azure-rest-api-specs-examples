```java
import com.azure.core.util.Context;

/** Samples for GalleryImageVersions Delete. */
public final class DeleteAGalleryImageVersion {
    /*
     * operationId: GalleryImageVersions_Delete
     * api-version: 2020-09-30
     * x-ms-examples: Delete a gallery image version.
     */
    /**
     * Sample code: Delete a gallery image version.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteAGalleryImageVersion(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryImageVersions()
            .delete("myResourceGroup", "myGalleryName", "myGalleryImageName", "1.0.0", Context.NONE);
    }
}
```