Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ContentType Delete. */
public final class Main {
    /*
     * operationId: ContentType_Delete
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementDeleteContentType
     */
    /**
     * Sample code: ApiManagementDeleteContentType.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementDeleteContentType(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.contentTypes().deleteWithResponse("rg1", "apimService1", "page", "*", Context.NONE);
    }
}
```
