```java
import com.azure.core.util.Context;

/** Samples for DedicatedHosts Get. */
public final class GetADedicatedHost {
    /*
     * operationId: DedicatedHosts_Get
     * api-version: 2021-04-01
     * x-ms-examples: Get a dedicated host.
     */
    /**
     * Sample code: Get a dedicated host.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getADedicatedHost(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDedicatedHosts()
            .getWithResponse("myResourceGroup", "myDedicatedHostGroup", "myHost", null, Context.NONE);
    }
}
```