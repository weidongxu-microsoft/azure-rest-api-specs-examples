```java
import com.azure.core.util.Context;

/** Samples for CloudServiceRoleInstances Delete. */
public final class DeleteCloudServiceRoleInstance {
    /*
     * operationId: CloudServiceRoleInstances_Delete
     * api-version: 2021-03-01
     * x-ms-examples: Delete Cloud Service Role Instance
     */
    /**
     * Sample code: Delete Cloud Service Role Instance.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteCloudServiceRoleInstance(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServiceRoleInstances()
            .delete("{roleInstance-name}", "ConstosoRG", "{cs-name}", Context.NONE);
    }
}
```