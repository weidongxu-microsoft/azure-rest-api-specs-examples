```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.RestorePointInner;
import com.azure.resourcemanager.compute.models.ApiEntityReference;
import java.util.Arrays;

/** Samples for RestorePoints Create. */
public final class CreateARestorePoint {
    /*
     * operationId: RestorePoints_Create
     * api-version: 2021-04-01
     * x-ms-examples: Create a restore point
     */
    /**
     * Sample code: Create a restore point.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createARestorePoint(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getRestorePoints()
            .create(
                "myResourceGroup",
                "rpcName",
                "rpName",
                new RestorePointInner()
                    .withExcludeDisks(
                        Arrays
                            .asList(
                                new ApiEntityReference()
                                    .withId(
                                        "/subscriptions/{subscription-id}/resourceGroups/myResourceGroup/providers/Microsoft.Compute/disks/disk123"))),
                Context.NONE);
    }
}
```