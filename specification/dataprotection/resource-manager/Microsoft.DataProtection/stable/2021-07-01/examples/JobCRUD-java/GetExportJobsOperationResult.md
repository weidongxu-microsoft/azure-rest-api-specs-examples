Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-dataprotection_1.0.0-beta.1/sdk/dataprotection/azure-resourcemanager-dataprotection/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ExportJobsOperationResult Get. */
public final class Main {
    /*
     * x-ms-original-file: specification/dataprotection/resource-manager/Microsoft.DataProtection/stable/2021-07-01/examples/JobCRUD/GetExportJobsOperationResult.json
     */
    /**
     * Sample code: Get Export Jobs Operation Result.
     *
     * @param manager Entry point to DataProtectionManager.
     */
    public static void getExportJobsOperationResult(
        com.azure.resourcemanager.dataprotection.DataProtectionManager manager) {
        manager
            .exportJobsOperationResults()
            .getWithResponse(
                "SwaggerTestRg", "NetSDKTestRsVault", "00000000-0000-0000-0000-000000000000", Context.NONE);
    }
}
```
