Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Tag DetachFromOperation. */
public final class Main {
    /*
     * operationId: Tag_DetachFromOperation
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementDeleteApiOperationTag
     */
    /**
     * Sample code: ApiManagementDeleteApiOperationTag.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementDeleteApiOperationTag(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .tags()
            .detachFromOperationWithResponse(
                "rg1",
                "apimService1",
                "59d5b28d1f7fab116c282650",
                "59d5b28d1f7fab116c282651",
                "59d5b28e1f7fab116402044e",
                Context.NONE);
    }
}
```
