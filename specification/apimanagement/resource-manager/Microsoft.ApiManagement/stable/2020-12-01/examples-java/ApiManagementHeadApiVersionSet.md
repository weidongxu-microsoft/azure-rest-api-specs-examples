Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ApiVersionSet GetEntityTag. */
public final class Main {
    /*
     * operationId: ApiVersionSet_GetEntityTag
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementHeadApiVersionSet
     */
    /**
     * Sample code: ApiManagementHeadApiVersionSet.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementHeadApiVersionSet(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apiVersionSets().getEntityTagWithResponse("rg1", "apimService1", "vs1", Context.NONE);
    }
}
```
