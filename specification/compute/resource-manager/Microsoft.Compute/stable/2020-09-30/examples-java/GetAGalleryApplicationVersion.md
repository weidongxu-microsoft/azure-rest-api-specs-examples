```java
import com.azure.core.util.Context;

/** Samples for GalleryApplicationVersions Get. */
public final class GetAGalleryApplicationVersion {
    /*
     * operationId: GalleryApplicationVersions_Get
     * api-version: 2020-09-30
     * x-ms-examples: Get a gallery Application Version.
     */
    /**
     * Sample code: Get a gallery Application Version.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAGalleryApplicationVersion(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryApplicationVersions()
            .getWithResponse(
                "myResourceGroup", "myGalleryName", "myGalleryApplicationName", "1.0.0", null, Context.NONE);
    }
}
```