```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.GalleryImageVersionPublishingProfile;
import com.azure.resourcemanager.compute.models.GalleryImageVersionStorageProfile;
import com.azure.resourcemanager.compute.models.GalleryImageVersionUpdate;
import com.azure.resourcemanager.compute.models.StorageAccountType;
import com.azure.resourcemanager.compute.models.TargetRegion;
import java.util.Arrays;

/** Samples for GalleryImageVersions Update. */
public final class UpdateASimpleGalleryImageVersionWithoutSourceId {
    /*
     * operationId: GalleryImageVersions_Update
     * api-version: 2020-09-30
     * x-ms-examples: Update a simple Gallery Image Version without source id.
     */
    /**
     * Sample code: Update a simple Gallery Image Version without source id.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void updateASimpleGalleryImageVersionWithoutSourceId(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryImageVersions()
            .update(
                "myResourceGroup",
                "myGalleryName",
                "myGalleryImageName",
                "1.0.0",
                new GalleryImageVersionUpdate()
                    .withPublishingProfile(
                        new GalleryImageVersionPublishingProfile()
                            .withTargetRegions(
                                Arrays
                                    .asList(
                                        new TargetRegion().withName("West US").withRegionalReplicaCount(1),
                                        new TargetRegion()
                                            .withName("East US")
                                            .withRegionalReplicaCount(2)
                                            .withStorageAccountType(StorageAccountType.STANDARD_ZRS))))
                    .withStorageProfile(new GalleryImageVersionStorageProfile()),
                Context.NONE);
    }
}
```