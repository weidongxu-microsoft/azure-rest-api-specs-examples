```java
import com.azure.core.util.Context;

/** Samples for GalleryImageVersions Get. */
public final class GetAGalleryImageVersionWithVhdAsSource {
    /*
     * operationId: GalleryImageVersions_Get
     * api-version: 2020-09-30
     * x-ms-examples: Get a gallery image version with vhd as a source.
     */
    /**
     * Sample code: Get a gallery image version with vhd as a source.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAGalleryImageVersionWithVhdAsASource(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryImageVersions()
            .getWithResponse("myResourceGroup", "myGalleryName", "myGalleryImageName", "1.0.0", null, Context.NONE);
    }
}
```