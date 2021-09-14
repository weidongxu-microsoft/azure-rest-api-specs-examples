Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Tag DetachFromProduct. */
public final class Main {
    /*
     * operationId: Tag_DetachFromProduct
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementDeleteProductTag
     */
    /**
     * Sample code: ApiManagementDeleteProductTag.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementDeleteProductTag(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .tags()
            .detachFromProductWithResponse(
                "rg1", "apimService1", "59d5b28d1f7fab116c282650", "59d5b28e1f7fab116402044e", Context.NONE);
    }
}
```
