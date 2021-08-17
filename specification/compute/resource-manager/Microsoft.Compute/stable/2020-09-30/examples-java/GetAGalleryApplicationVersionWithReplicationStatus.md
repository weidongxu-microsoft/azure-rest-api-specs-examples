```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.ReplicationStatusTypes;

/** Samples for GalleryApplicationVersions Get. */
public final class GetAGalleryApplicationVersionWithReplicationStatus {
    /*
     * operationId: GalleryApplicationVersions_Get
     * api-version: 2020-09-30
     * x-ms-examples: Get a gallery Application Version with replication status.
     */
    /**
     * Sample code: Get a gallery Application Version with replication status.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAGalleryApplicationVersionWithReplicationStatus(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getGalleryApplicationVersions()
            .getWithResponse(
                "myResourceGroup",
                "myGalleryName",
                "myGalleryApplicationName",
                "1.0.0",
                ReplicationStatusTypes.REPLICATION_STATUS,
                Context.NONE);
    }
}
```