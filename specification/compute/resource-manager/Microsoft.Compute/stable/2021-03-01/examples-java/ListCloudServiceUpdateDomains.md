```java
import com.azure.core.util.Context;

/** Samples for CloudServicesUpdateDomain ListUpdateDomains. */
public final class ListCloudServiceUpdateDomains {
    /*
     * operationId: CloudServicesUpdateDomain_ListUpdateDomains
     * api-version: 2021-03-01
     * x-ms-examples: List Update Domains in Cloud Service
     */
    /**
     * Sample code: List Update Domains in Cloud Service.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listUpdateDomainsInCloudService(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServicesUpdateDomains()
            .listUpdateDomains("ConstosoRG", "{cs-name}", Context.NONE);
    }
}
```