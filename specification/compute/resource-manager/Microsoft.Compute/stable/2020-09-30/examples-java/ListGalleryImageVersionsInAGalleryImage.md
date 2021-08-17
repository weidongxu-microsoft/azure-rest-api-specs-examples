```java
import com.azure.core.util.Context;

/** Samples for GalleryImageVersions ListByGalleryImage. */
public final class ListGalleryImageVersionsInAGalleryImage {
    /*
     * operationId: GalleryImageVersions_ListByGalleryImage
     * api-version: 2020-09-30
     * x-ms-examples: List gallery image versions in a gallery image definition.
     */
    /**
     * Sample code: List gallery image versions in a gallery image definition.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listGalleryImageVersionsInAGalleryImageDefinition(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryImageVersions()
            .listByGalleryImage("myResourceGroup", "myGalleryName", "myGalleryImageName", Context.NONE);
    }
}
```