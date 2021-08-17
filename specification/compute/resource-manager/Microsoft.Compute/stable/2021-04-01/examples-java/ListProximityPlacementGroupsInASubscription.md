```java
import com.azure.core.util.Context;

/** Samples for ProximityPlacementGroups List. */
public final class ListProximityPlacementGroupsInASubscription {
    /*
     * operationId: ProximityPlacementGroups_ListBySubscription
     * api-version: 2021-04-01
     * x-ms-examples: Create a proximity placement group.
     */
    /**
     * Sample code: Create a proximity placement group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createAProximityPlacementGroup(com.azure.resourcemanager.AzureResourceManager azure) {
        azure.virtualMachines().manager().serviceClient().getProximityPlacementGroups().list(Context.NONE);
    }
}
```