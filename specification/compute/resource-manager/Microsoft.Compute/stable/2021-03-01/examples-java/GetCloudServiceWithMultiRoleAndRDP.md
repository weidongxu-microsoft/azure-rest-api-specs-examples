```java
import com.azure.core.util.Context;

/** Samples for CloudServices GetByResourceGroup. */
public final class GetCloudServiceWithMultiRoleAndRDP {
    /*
     * operationId: CloudServices_Get
     * api-version: 2021-03-01
     * x-ms-examples: Get Cloud Service with Multiple Roles and RDP Extension
     */
    /**
     * Sample code: Get Cloud Service with Multiple Roles and RDP Extension.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getCloudServiceWithMultipleRolesAndRDPExtension(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServices()
            .getByResourceGroupWithResponse("ConstosoRG", "{cs-name}", Context.NONE);
    }
}
```