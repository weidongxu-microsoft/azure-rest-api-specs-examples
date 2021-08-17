```java
import com.azure.core.util.Context;

/** Samples for CloudServices GetInstanceView. */
public final class GetCloudServiceInstanceViewWithMultiRole {
    /*
     * operationId: CloudServices_GetInstanceView
     * api-version: 2021-03-01
     * x-ms-examples: Get Cloud Service Instance View with Multiple Roles
     */
    /**
     * Sample code: Get Cloud Service Instance View with Multiple Roles.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getCloudServiceInstanceViewWithMultipleRoles(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServices()
            .getInstanceViewWithResponse("ConstosoRG", "{cs-name}", Context.NONE);
    }
}
```