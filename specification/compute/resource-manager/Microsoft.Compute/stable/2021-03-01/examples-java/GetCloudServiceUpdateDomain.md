```java
import com.azure.core.util.Context;

/** Samples for CloudServicesUpdateDomain GetUpdateDomain. */
public final class GetCloudServiceUpdateDomain {
    /*
     * operationId: CloudServicesUpdateDomain_GetUpdateDomain
     * api-version: 2021-03-01
     * x-ms-examples: Get Cloud Service Update Domain
     */
    /**
     * Sample code: Get Cloud Service Update Domain.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getCloudServiceUpdateDomain(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServicesUpdateDomains()
            .getUpdateDomainWithResponse("ConstosoRG", "{cs-name}", 1, Context.NONE);
    }
}
```