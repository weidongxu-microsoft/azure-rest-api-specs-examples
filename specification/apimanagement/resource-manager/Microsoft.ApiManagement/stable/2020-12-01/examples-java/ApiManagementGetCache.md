Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Cache Get. */
public final class Main {
    /*
     * operationId: Cache_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetCache
     */
    /**
     * Sample code: ApiManagementGetCache.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetCache(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.caches().getWithResponse("rg1", "apimService1", "c1", Context.NONE);
    }
}
```
