Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Operation ListByTags. */
public final class Main {
    /*
     * operationId: Operation_ListByTags
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListApiOperationsByTags
     */
    /**
     * Sample code: ApiManagementListApiOperationsByTags.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListApiOperationsByTags(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.operations().listByTags("rg1", "apimService1", "a1", null, null, null, null, Context.NONE);
    }
}
```
