Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ApiVersionSet Get. */
public final class Main {
    /*
     * operationId: ApiVersionSet_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetApiVersionSet
     */
    /**
     * Sample code: ApiManagementGetApiVersionSet.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetApiVersionSet(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apiVersionSets().getWithResponse("rg1", "apimService1", "vs1", Context.NONE);
    }
}
```
