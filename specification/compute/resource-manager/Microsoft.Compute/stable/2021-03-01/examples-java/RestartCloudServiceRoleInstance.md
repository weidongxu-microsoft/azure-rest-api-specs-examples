```java
import com.azure.core.util.Context;

/** Samples for CloudServiceRoleInstances Restart. */
public final class RestartCloudServiceRoleInstance {
    /*
     * operationId: CloudServiceRoleInstances_Restart
     * api-version: 2021-03-01
     * x-ms-examples: Restart Cloud Service Role Instance
     */
    /**
     * Sample code: Restart Cloud Service Role Instance.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void restartCloudServiceRoleInstance(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServiceRoleInstances()
            .restart("{roleInstance-name}", "ConstosoRG", "{cs-name}", Context.NONE);
    }
}
```