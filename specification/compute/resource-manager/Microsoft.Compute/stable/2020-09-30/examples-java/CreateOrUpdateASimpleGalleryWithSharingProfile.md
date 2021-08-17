```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.GalleryInner;
import com.azure.resourcemanager.compute.models.GallerySharingPermissionTypes;
import com.azure.resourcemanager.compute.models.SharingProfile;

/** Samples for Galleries CreateOrUpdate. */
public final class CreateOrUpdateASimpleGalleryWithSharingProfile {
    /*
     * operationId: Galleries_CreateOrUpdate
     * api-version: 2020-09-30
     * x-ms-examples: Create or update a simple gallery with sharing profile.
     */
    /**
     * Sample code: Create or update a simple gallery with sharing profile.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createOrUpdateASimpleGalleryWithSharingProfile(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleries()
            .createOrUpdate(
                "myResourceGroup",
                "myGalleryName",
                new GalleryInner()
                    .withLocation("West US")
                    .withDescription("This is the gallery description.")
                    .withSharingProfile(new SharingProfile().withPermissions(GallerySharingPermissionTypes.GROUPS)),
                Context.NONE);
    }
}
```