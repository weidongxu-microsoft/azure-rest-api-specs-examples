```java
import com.azure.core.util.Context;

/** Samples for CloudServiceOperatingSystems GetOSFamily. */
public final class GetCloudServiceOSFamily {
    /*
     * operationId: CloudServiceOperatingSystems_GetOSFamily
     * api-version: 2021-03-01
     * x-ms-examples: Get Cloud Service OS Family
     */
    /**
     * Sample code: Get Cloud Service OS Family.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getCloudServiceOSFamily(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServiceOperatingSystems()
            .getOSFamilyWithResponse("westus2", "3", Context.NONE);
    }
}
```