```java
import com.azure.core.util.Context;

/** Samples for CloudServiceRoles List. */
public final class ListCloudServiceRoles {
    /*
     * operationId: CloudServiceRoles_List
     * api-version: 2021-03-01
     * x-ms-examples: List Roles in a Cloud Service
     */
    /**
     * Sample code: List Roles in a Cloud Service.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listRolesInACloudService(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServiceRoles()
            .list("ConstosoRG", "{cs-name}", Context.NONE);
    }
}
```