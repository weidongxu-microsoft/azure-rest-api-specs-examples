```java
import com.azure.core.util.Context;

/** Samples for CloudServiceOperatingSystems GetOSVersion. */
public final class GetCloudServiceOSVersion {
    /*
     * operationId: CloudServiceOperatingSystems_GetOSVersion
     * api-version: 2021-03-01
     * x-ms-examples: Get Cloud Service OS Version
     */
    /**
     * Sample code: Get Cloud Service OS Version.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getCloudServiceOSVersion(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServiceOperatingSystems()
            .getOSVersionWithResponse("westus2", "WA-GUEST-OS-3.90_202010-02", Context.NONE);
    }
}
```