Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Api ListByTags. */
public final class Main {
    /*
     * operationId: Api_ListByTags
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListApisByTags
     */
    /**
     * Sample code: ApiManagementListApisByTags.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListApisByTags(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apis().listByTags("rg1", "apimService1", null, null, null, null, Context.NONE);
    }
}
```
