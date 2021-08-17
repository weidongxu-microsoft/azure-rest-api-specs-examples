```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.GalleryUpdate;

/** Samples for Galleries Update. */
public final class UpdateASimpleGallery {
    /*
     * operationId: Galleries_Update
     * api-version: 2020-09-30
     * x-ms-examples: Update a simple gallery.
     */
    /**
     * Sample code: Update a simple gallery.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void updateASimpleGallery(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleries()
            .update(
                "myResourceGroup",
                "myGalleryName",
                new GalleryUpdate().withDescription("This is the gallery description."),
                Context.NONE);
    }
}
```