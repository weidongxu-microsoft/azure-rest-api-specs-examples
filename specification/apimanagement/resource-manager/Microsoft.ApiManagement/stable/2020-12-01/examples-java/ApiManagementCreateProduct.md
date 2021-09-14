Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
/** Samples for Product CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Product_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateProduct
     */
    /**
     * Sample code: ApiManagementCreateProduct.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateProduct(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .products()
            .define("testproduct")
            .withExistingService("rg1", "apimService1")
            .withDisplayName("Test Template ProductName 4")
            .create();
    }
}
```
