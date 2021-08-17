```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.GalleryInner;

/** Samples for Galleries CreateOrUpdate. */
public final class CreateOrUpdateASimpleGallery {
    /*
     * operationId: Galleries_CreateOrUpdate
     * api-version: 2020-09-30
     * x-ms-examples: Create or update a simple gallery.
     */
    /**
     * Sample code: Create or update a simple gallery.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createOrUpdateASimpleGallery(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleries()
            .createOrUpdate(
                "myResourceGroup",
                "myGalleryName",
                new GalleryInner().withLocation("West US").withDescription("This is the gallery description."),
                Context.NONE);
    }
}
```