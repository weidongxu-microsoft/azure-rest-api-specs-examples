Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ContentItem CreateOrUpdate. */
public final class Main {
    /*
     * operationId: ContentItem_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateContentTypeContentItem
     */
    /**
     * Sample code: ApiManagementCreateContentTypeContentItem.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateContentTypeContentItem(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .contentItems()
            .createOrUpdateWithResponse(
                "rg1", "apimService1", "page", "4e3cf6a5-574a-ba08-1f23-2e7a38faa6d8", null, Context.NONE);
    }
}
```
