Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-dataprotection_1.0.0-beta.1/sdk/dataprotection/azure-resourcemanager-dataprotection/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Jobs Get. */
public final class Main {
    /*
     * x-ms-original-file: specification/dataprotection/resource-manager/Microsoft.DataProtection/stable/2021-07-01/examples/JobCRUD/GetJob.json
     */
    /**
     * Sample code: Get Job.
     *
     * @param manager Entry point to DataProtectionManager.
     */
    public static void getJob(com.azure.resourcemanager.dataprotection.DataProtectionManager manager) {
        manager
            .jobs()
            .getWithResponse("BugBash1", "BugBashVaultForCCYv11", "3c60cb49-63e8-4b21-b9bd-26277b3fdfae", Context.NONE);
    }
}
```
