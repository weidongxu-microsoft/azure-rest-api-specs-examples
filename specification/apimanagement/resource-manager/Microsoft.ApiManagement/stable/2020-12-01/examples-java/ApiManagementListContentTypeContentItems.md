Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ContentItem ListByService. */
public final class Main {
    /*
     * operationId: ContentItem_ListByService
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListContentTypeContentItems
     */
    /**
     * Sample code: ApiManagementListContentTypeContentItems.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListContentTypeContentItems(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.contentItems().listByService("rg1", "apimService1", "page", Context.NONE);
    }
}
```
