```java
import com.azure.core.util.Context;

/** Samples for CapacityReservations ListByCapacityReservationGroup. */
public final class ListCapacityReservationsInReservationGroup {
    /*
     * operationId: CapacityReservations_ListByCapacityReservationGroup
     * api-version: 2021-04-01
     * x-ms-examples: List capacity reservations in reservation group.
     */
    /**
     * Sample code: List capacity reservations in reservation group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listCapacityReservationsInReservationGroup(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCapacityReservations()
            .listByCapacityReservationGroup("myResourceGroup", "myCapacityReservationGroup", Context.NONE);
    }
}
```