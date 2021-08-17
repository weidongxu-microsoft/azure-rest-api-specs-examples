```java
import com.azure.core.util.Context;

/** Samples for CloudServiceRoles Get. */
public final class GetCloudServiceRole {
    /*
     * operationId: CloudServiceRoles_Get
     * api-version: 2021-03-01
     * x-ms-examples: Get Cloud Service Role
     */
    /**
     * Sample code: Get Cloud Service Role.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getCloudServiceRole(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServiceRoles()
            .getWithResponse("{role-name}", "ConstosoRG", "{cs-name}", Context.NONE);
    }
}
```