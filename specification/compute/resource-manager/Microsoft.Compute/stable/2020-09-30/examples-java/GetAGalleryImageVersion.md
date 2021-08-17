```java
import com.azure.core.util.Context;

/** Samples for GalleryImageVersions Get. */
public final class GetAGalleryImageVersion {
    /*
     * operationId: GalleryImageVersions_Get
     * api-version: 2020-09-30
     * x-ms-examples: Get a gallery image version.
     */
    /**
     * Sample code: Get a gallery image version.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAGalleryImageVersion(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryImageVersions()
            .getWithResponse("myResourceGroup", "myGalleryName", "myGalleryImageName", "1.0.0", null, Context.NONE);
    }
}
```