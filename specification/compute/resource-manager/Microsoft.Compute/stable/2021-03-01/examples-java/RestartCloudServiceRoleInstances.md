```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.RoleInstances;
import java.util.Arrays;

/** Samples for CloudServices Restart. */
public final class RestartCloudServiceRoleInstances {
    /*
     * operationId: CloudServices_Restart
     * api-version: 2021-03-01
     * x-ms-examples: Restart Cloud Service Role Instances
     */
    /**
     * Sample code: Restart Cloud Service Role Instances.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void restartCloudServiceRoleInstances(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServices()
            .restart(
                "ConstosoRG",
                "{cs-name}",
                new RoleInstances().withRoleInstances(Arrays.asList("ContosoFrontend_IN_0", "ContosoBackend_IN_1")),
                Context.NONE);
    }
}
```