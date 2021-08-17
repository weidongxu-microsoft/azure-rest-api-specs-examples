```java
import com.azure.core.util.Context;

/** Samples for CloudServiceRoleInstances Get. */
public final class GetCloudServiceRoleInstance {
    /*
     * operationId: CloudServiceRoleInstances_Get
     * api-version: 2021-03-01
     * x-ms-examples: Get Cloud Service Role Instance
     */
    /**
     * Sample code: Get Cloud Service Role Instance.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getCloudServiceRoleInstance(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServiceRoleInstances()
            .getWithResponse("{roleInstance-name}", "ConstosoRG", "{cs-name}", null, Context.NONE);
    }
}
```