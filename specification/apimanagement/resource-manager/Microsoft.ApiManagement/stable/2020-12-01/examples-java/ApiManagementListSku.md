Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ApiManagementSkus List. */
public final class Main {
    /*
     * operationId: ApiManagementSkus_List
     * api-version: 2020-12-01
     * x-ms-examples: Lists all available Resource SKUs
     */
    /**
     * Sample code: Lists all available Resource SKUs.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void listsAllAvailableResourceSKUs(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apiManagementSkus().list(Context.NONE);
    }
}
```
