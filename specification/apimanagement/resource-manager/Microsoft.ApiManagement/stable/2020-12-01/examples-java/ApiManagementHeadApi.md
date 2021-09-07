Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Api GetEntityTag. */
public final class Main {
    /*
     * operationId: Api_GetEntityTag
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementHeadApi
     */
    /**
     * Sample code: ApiManagementHeadApi.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementHeadApi(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apis().getEntityTagWithResponse("rg1", "apimService1", "57d1f7558aa04f15146d9d8a", Context.NONE);
    }
}
```
