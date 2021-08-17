```java
import com.azure.core.util.Context;

/** Samples for ProximityPlacementGroups Delete. */
public final class DeleteAProximityPlacementGroup {
    /*
     * operationId: ProximityPlacementGroups_Delete
     * api-version: 2021-04-01
     * x-ms-examples: Create a proximity placement group.
     */
    /**
     * Sample code: Create a proximity placement group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createAProximityPlacementGroup(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getProximityPlacementGroups()
            .deleteWithResponse("myResourceGroup", "myProximityPlacementGroup", Context.NONE);
    }
}
```