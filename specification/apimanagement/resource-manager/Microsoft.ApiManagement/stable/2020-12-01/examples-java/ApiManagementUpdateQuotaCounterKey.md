Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.QuotaCounterValueUpdateContract;

/** Samples for QuotaByCounterKeys Update. */
public final class Main {
    /*
     * operationId: QuotaByCounterKeys_Update
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementUpdateQuotaCounterKey
     */
    /**
     * Sample code: ApiManagementUpdateQuotaCounterKey.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementUpdateQuotaCounterKey(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .quotaByCounterKeys()
            .updateWithResponse(
                "rg1",
                "apimService1",
                "ba",
                new QuotaCounterValueUpdateContract().withCallsCount(0).withKbTransferred(2.5630078125),
                Context.NONE);
    }
}
```
