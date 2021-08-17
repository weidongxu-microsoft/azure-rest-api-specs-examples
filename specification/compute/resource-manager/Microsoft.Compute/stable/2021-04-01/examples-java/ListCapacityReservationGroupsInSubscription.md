```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.ExpandTypesForGetCapacityReservationGroups;

/** Samples for CapacityReservationGroups List. */
public final class ListCapacityReservationGroupsInSubscription {
    /*
     * operationId: CapacityReservationGroups_ListBySubscription
     * api-version: 2021-04-01
     * x-ms-examples: List capacity reservation groups in subscription.
     */
    /**
     * Sample code: List capacity reservation groups in subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listCapacityReservationGroupsInSubscription(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCapacityReservationGroups()
            .list(ExpandTypesForGetCapacityReservationGroups.VIRTUAL_MACHINES_REF, Context.NONE);
    }
}
```