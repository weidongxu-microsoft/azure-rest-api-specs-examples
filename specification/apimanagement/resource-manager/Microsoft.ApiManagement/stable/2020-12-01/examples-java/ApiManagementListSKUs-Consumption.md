Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ApiManagementServiceSkus ListAvailableServiceSkus. */
public final class Main {
    /*
     * operationId: ApiManagementServiceSkus_ListAvailableServiceSkus
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListSKUs-Consumption
     */
    /**
     * Sample code: ApiManagementListSKUs-Consumption.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListSKUsConsumption(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apiManagementServiceSkus().listAvailableServiceSkus("rg1", "apimService1", Context.NONE);
    }
}
```
