```java
import com.azure.core.util.Context;

/** Samples for CloudServiceRoleInstances Reimage. */
public final class ReimageCloudServiceRoleInstance {
    /*
     * operationId: CloudServiceRoleInstances_Reimage
     * api-version: 2021-03-01
     * x-ms-examples: Reimage Cloud Service Role Instance
     */
    /**
     * Sample code: Reimage Cloud Service Role Instance.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void reimageCloudServiceRoleInstance(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServiceRoleInstances()
            .reimage("{roleInstance-name}", "ConstosoRG", "{cs-name}", Context.NONE);
    }
}
```