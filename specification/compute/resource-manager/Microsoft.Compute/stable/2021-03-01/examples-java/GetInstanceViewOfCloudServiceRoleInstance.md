```java
import com.azure.core.util.Context;

/** Samples for CloudServiceRoleInstances GetInstanceView. */
public final class GetInstanceViewOfCloudServiceRoleInstance {
    /*
     * operationId: CloudServiceRoleInstances_GetInstanceView
     * api-version: 2021-03-01
     * x-ms-examples: Get Instance View of Cloud Service Role Instance
     */
    /**
     * Sample code: Get Instance View of Cloud Service Role Instance.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getInstanceViewOfCloudServiceRoleInstance(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServiceRoleInstances()
            .getInstanceViewWithResponse("{roleInstance-name}", "ConstosoRG", "{cs-name}", Context.NONE);
    }
}
```