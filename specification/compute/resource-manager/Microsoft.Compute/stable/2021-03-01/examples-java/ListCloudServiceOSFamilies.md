```java
import com.azure.core.util.Context;

/** Samples for CloudServiceOperatingSystems ListOSFamilies. */
public final class ListCloudServiceOSFamilies {
    /*
     * operationId: CloudServiceOperatingSystems_ListOSFamilies
     * api-version: 2021-03-01
     * x-ms-examples: List Cloud Service OS Families in a subscription
     */
    /**
     * Sample code: List Cloud Service OS Families in a subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listCloudServiceOSFamiliesInASubscription(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServiceOperatingSystems()
            .listOSFamilies("westus2", Context.NONE);
    }
}
```