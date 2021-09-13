Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ApiVersionSet Delete. */
public final class Main {
    /*
     * operationId: ApiVersionSet_Delete
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementDeleteApiVersionSet
     */
    /**
     * Sample code: ApiManagementDeleteApiVersionSet.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementDeleteApiVersionSet(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apiVersionSets().deleteWithResponse("rg1", "apimService1", "a1", "*", Context.NONE);
    }
}
```
