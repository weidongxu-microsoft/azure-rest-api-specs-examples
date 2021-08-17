```java
import com.azure.core.util.Context;

/** Samples for RestorePoints Get. */
public final class GetRestorePoint {
    /*
     * operationId: RestorePoints_Get
     * api-version: 2021-04-01
     * x-ms-examples: Get a restore point
     */
    /**
     * Sample code: Get a restore point.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getARestorePoint(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getRestorePoints()
            .getWithResponse("myResourceGroup", "rpcName", "rpName", Context.NONE);
    }
}
```