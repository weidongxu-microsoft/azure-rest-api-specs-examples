```java
import com.azure.core.util.Context;

/** Samples for Snapshots GetByResourceGroup. */
public final class GetInformationAboutASnapshot {
    /*
     * operationId: Snapshots_Get
     * api-version: 2020-12-01
     * x-ms-examples: Get information about a snapshot.
     */
    /**
     * Sample code: Get information about a snapshot.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getInformationAboutASnapshot(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getSnapshots()
            .getByResourceGroupWithResponse("myResourceGroup", "mySnapshot", Context.NONE);
    }
}
```