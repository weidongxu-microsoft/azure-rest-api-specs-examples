```java
import com.azure.core.util.Context;

/** Samples for GalleryApplicationVersions ListByGalleryApplication. */
public final
class ListGalleryApplicationVersionsInAGalleryApplication {
    /*
     * operationId: GalleryApplicationVersions_ListByGalleryApplication
     * api-version: 2020-09-30
     * x-ms-examples: List gallery Application Versions in a gallery Application Definition.
     */
    /**
     * Sample code: List gallery Application Versions in a gallery Application Definition.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listGalleryApplicationVersionsInAGalleryApplicationDefinition(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryApplicationVersions()
            .listByGalleryApplication("myResourceGroup", "myGalleryName", "myGalleryApplicationName", Context.NONE);
    }
}
```