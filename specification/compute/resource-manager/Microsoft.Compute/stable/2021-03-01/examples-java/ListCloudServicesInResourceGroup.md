```java
import com.azure.core.util.Context;

/** Samples for CloudServices ListByResourceGroup. */
public final class ListCloudServicesInResourceGroup {
    /*
     * operationId: CloudServices_List
     * api-version: 2021-03-01
     * x-ms-examples: List Cloud Services in a Resource Group
     */
    /**
     * Sample code: List Cloud Services in a Resource Group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listCloudServicesInAResourceGroup(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServices()
            .listByResourceGroup("ConstosoRG", Context.NONE);
    }
}
```