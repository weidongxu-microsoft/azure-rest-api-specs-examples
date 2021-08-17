```java
import com.azure.core.util.Context;

/** Samples for CloudServiceRoleInstances Rebuild. */
public final class RebuildCloudServiceRoleInstance {
    /*
     * operationId: CloudServiceRoleInstances_Rebuild
     * api-version: 2021-03-01
     * x-ms-examples: Rebuild Cloud Service Role Instance
     */
    /**
     * Sample code: Rebuild Cloud Service Role Instance.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void rebuildCloudServiceRoleInstance(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServiceRoleInstances()
            .rebuild("{roleInstance-name}", "ConstosoRG", "{cs-name}", Context.NONE);
    }
}
```