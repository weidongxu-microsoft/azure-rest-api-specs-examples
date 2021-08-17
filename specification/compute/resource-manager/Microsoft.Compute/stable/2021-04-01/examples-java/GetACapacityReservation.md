```java
import com.azure.core.util.Context;

/** Samples for CapacityReservations Get. */
public final class GetACapacityReservation {
    /*
     * operationId: CapacityReservations_Get
     * api-version: 2021-04-01
     * x-ms-examples: Get a capacity reservation.
     */
    /**
     * Sample code: Get a capacity reservation.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getACapacityReservation(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCapacityReservations()
            .getWithResponse(
                "myResourceGroup", "myCapacityReservationGroup", "myCapacityReservation", null, Context.NONE);
    }
}
```