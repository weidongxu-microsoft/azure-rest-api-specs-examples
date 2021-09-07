Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for ContentItem GetEntityTag. */
public final class Main {
    /*
     * operationId: ContentItem_GetEntityTag
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementHeadContentTypeContentItem
     */
    /**
     * Sample code: ApiManagementHeadContentTypeContentItem.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementHeadContentTypeContentItem(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .contentItems()
            .getEntityTagWithResponse(
                "rg1", "apimService1", "page", "4e3cf6a5-574a-ba08-1f23-2e7a38faa6d8", Context.NONE);
    }
}
```
