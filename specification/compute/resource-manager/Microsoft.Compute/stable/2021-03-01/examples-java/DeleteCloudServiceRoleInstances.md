```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.RoleInstances;
import java.util.Arrays;

/** Samples for CloudServices DeleteInstances. */
public final class DeleteCloudServiceRoleInstances {
    /*
     * operationId: CloudServices_DeleteInstances
     * api-version: 2021-03-01
     * x-ms-examples: Delete Cloud Service Role Instances
     */
    /**
     * Sample code: Delete Cloud Service Role Instances.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteCloudServiceRoleInstances(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServices()
            .deleteInstances(
                "ConstosoRG",
                "{cs-name}",
                new RoleInstances().withRoleInstances(Arrays.asList("ContosoFrontend_IN_0", "ContosoBackend_IN_1")),
                Context.NONE);
    }
}
```