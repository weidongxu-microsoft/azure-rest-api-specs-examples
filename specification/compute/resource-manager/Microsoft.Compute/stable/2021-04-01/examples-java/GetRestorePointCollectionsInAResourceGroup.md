```java
import com.azure.core.util.Context;

/** Samples for RestorePointCollections ListByResourceGroup. */
public final
class GetRestorePointCollectionsInAResourceGroup {
    /*
     * operationId: RestorePointCollections_List
     * api-version: 2021-04-01
     * x-ms-examples: Gets the list of restore point collections in a resource group.
     */
    /**
     * Sample code: Gets the list of restore point collections in a resource group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getsTheListOfRestorePointCollectionsInAResourceGroup(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getRestorePointCollections()
            .listByResourceGroup("myResourceGroup", Context.NONE);
    }
}
```