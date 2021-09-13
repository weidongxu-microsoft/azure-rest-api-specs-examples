Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ProductGroup ListByProduct. */
public final class Main {
    /*
     * operationId: ProductGroup_ListByProduct
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListProductGroups
     */
    /**
     * Sample code: ApiManagementListProductGroups.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListProductGroups(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .productGroups()
            .listByProduct("rg1", "apimService1", "5600b57e7e8880006a060002", null, null, null, Context.NONE);
    }
}
```
