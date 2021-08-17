```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.RoleInstances;
import java.util.Arrays;

/** Samples for CloudServices Reimage. */
public final class ReimageCloudServiceRoleInstances {
    /*
     * operationId: CloudServices_Reimage
     * api-version: 2021-03-01
     * x-ms-examples: Reimage Cloud Service Role Instances
     */
    /**
     * Sample code: Reimage Cloud Service Role Instances.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void reimageCloudServiceRoleInstances(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServices()
            .reimage(
                "ConstosoRG",
                "{cs-name}",
                new RoleInstances().withRoleInstances(Arrays.asList("ContosoFrontend_IN_0", "ContosoBackend_IN_1")),
                Context.NONE);
    }
}
```