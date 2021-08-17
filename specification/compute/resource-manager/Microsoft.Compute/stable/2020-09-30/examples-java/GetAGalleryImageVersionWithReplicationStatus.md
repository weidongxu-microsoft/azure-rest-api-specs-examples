```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.ReplicationStatusTypes;

/** Samples for GalleryImageVersions Get. */
public final class GetAGalleryImageVersionWithReplicationStatus {
    /*
     * operationId: GalleryImageVersions_Get
     * api-version: 2020-09-30
     * x-ms-examples: Get a gallery image version with replication status.
     */
    /**
     * Sample code: Get a gallery image version with replication status.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAGalleryImageVersionWithReplicationStatus(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryImageVersions()
            .getWithResponse(
                "myResourceGroup",
                "myGalleryName",
                "myGalleryImageName",
                "1.0.0",
                ReplicationStatusTypes.REPLICATION_STATUS,
                Context.NONE);
    }
}
```