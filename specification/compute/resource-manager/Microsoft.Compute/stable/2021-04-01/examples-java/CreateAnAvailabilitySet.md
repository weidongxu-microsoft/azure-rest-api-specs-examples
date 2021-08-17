```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.AvailabilitySetInner;

/** Samples for AvailabilitySets CreateOrUpdate. */
public final class CreateAnAvailabilitySet {
    /*
     * operationId: AvailabilitySets_CreateOrUpdate
     * api-version: 2021-04-01
     * x-ms-examples: Create an availability set.
     */
    /**
     * Sample code: Create an availability set.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createAnAvailabilitySet(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getAvailabilitySets()
            .createOrUpdateWithResponse(
                "myResourceGroup",
                "myAvailabilitySet",
                new AvailabilitySetInner()
                    .withLocation("westus")
                    .withPlatformUpdateDomainCount(20)
                    .withPlatformFaultDomainCount(2),
                Context.NONE);
    }
}
```