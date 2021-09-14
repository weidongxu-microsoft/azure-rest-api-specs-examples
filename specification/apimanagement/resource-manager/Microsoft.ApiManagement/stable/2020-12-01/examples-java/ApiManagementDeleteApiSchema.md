Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ApiSchema Delete. */
public final class Main {
    /*
     * operationId: ApiSchema_Delete
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementDeleteApiSchema
     */
    /**
     * Sample code: ApiManagementDeleteApiSchema.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementDeleteApiSchema(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apiSchemas()
            .deleteWithResponse(
                "rg1", "apimService1", "59d5b28d1f7fab116c282650", "59d5b28e1f7fab116402044e", "*", null, Context.NONE);
    }
}
```
