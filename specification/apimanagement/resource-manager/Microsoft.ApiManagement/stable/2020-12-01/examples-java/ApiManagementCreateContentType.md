Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ContentType CreateOrUpdate. */
public final class Main {
    /*
     * operationId: ContentType_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateContentType
     */
    /**
     * Sample code: ApiManagementCreateContentType.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateContentType(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.contentTypes().createOrUpdateWithResponse("rg1", "apimService1", "page", null, Context.NONE);
    }
}
```
