```java
import com.azure.core.util.Context;

/** Samples for CapacityReservationGroups GetByResourceGroup. */
public final class GetACapacityReservationGroup {
    /*
     * operationId: CapacityReservationGroups_Get
     * api-version: 2021-04-01
     * x-ms-examples: Get a capacity reservation Group.
     */
    /**
     * Sample code: Get a capacity reservation Group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getACapacityReservationGroup(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCapacityReservationGroups()
            .getByResourceGroupWithResponse("myResourceGroup", "myCapacityReservationGroup", null, Context.NONE);
    }
}
```