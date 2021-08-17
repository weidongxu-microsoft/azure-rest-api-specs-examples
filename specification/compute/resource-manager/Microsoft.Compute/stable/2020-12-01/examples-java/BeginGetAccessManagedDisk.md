```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.AccessLevel;
import com.azure.resourcemanager.compute.models.GrantAccessData;

/** Samples for Disks GrantAccess. */
public final class BeginGetAccessManagedDisk {
    /*
     * operationId: Disks_GrantAccess
     * api-version: 2020-12-01
     * x-ms-examples: Get a sas on a managed disk.
     */
    /**
     * Sample code: Get a sas on a managed disk.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getASasOnAManagedDisk(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDisks()
            .grantAccess(
                "myResourceGroup",
                "myDisk",
                new GrantAccessData().withAccess(AccessLevel.READ).withDurationInSeconds(300),
                Context.NONE);
    }
}
```