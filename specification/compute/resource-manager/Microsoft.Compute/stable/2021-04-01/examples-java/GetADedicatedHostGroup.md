```java
import com.azure.core.util.Context;

/** Samples for DedicatedHostGroups GetByResourceGroup. */
public final class GetADedicatedHostGroup {
    /*
     * operationId: DedicatedHostGroups_Get
     * api-version: 2021-04-01
     * x-ms-examples: Create a dedicated host group.
     */
    /**
     * Sample code: Create a dedicated host group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createADedicatedHostGroup(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDedicatedHostGroups()
            .getByResourceGroupWithResponse("myResourceGroup", "myDedicatedHostGroup", null, Context.NONE);
    }
}
```