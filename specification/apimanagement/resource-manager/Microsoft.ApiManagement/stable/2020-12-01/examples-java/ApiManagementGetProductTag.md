Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Tag GetByProduct. */
public final class Main {
    /*
     * operationId: Tag_GetByProduct
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetProductTag
     */
    /**
     * Sample code: ApiManagementGetProductTag.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetProductTag(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .tags()
            .getByProductWithResponse(
                "rg1", "apimService1", "59d6bb8f1f7fab13dc67ec9b", "59306a29e4bbd510dc24e5f9", Context.NONE);
    }
}
```
