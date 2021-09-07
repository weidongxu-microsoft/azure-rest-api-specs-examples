Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for ApiSchema ListByApi. */
public final class Main {
    /*
     * operationId: ApiSchema_ListByApi
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListApiSchemas
     */
    /**
     * Sample code: ApiManagementListApiSchemas.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListApiSchemas(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apiSchemas()
            .listByApi("rg1", "apimService1", "59d5b28d1f7fab116c282650", null, null, null, Context.NONE);
    }
}
```
