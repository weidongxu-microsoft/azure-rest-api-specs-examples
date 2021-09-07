Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Product ListByService. */
public final class Main {
    /*
     * operationId: Product_ListByService
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListProducts
     */
    /**
     * Sample code: ApiManagementListProducts.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListProducts(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.products().listByService("rg1", "apimService1", null, null, null, null, null, Context.NONE);
    }
}
```
