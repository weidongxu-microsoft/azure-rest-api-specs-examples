Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for ApiTagDescription Get. */
public final class Main {
    /*
     * operationId: ApiTagDescription_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetApiTagDescription
     */
    /**
     * Sample code: ApiManagementGetApiTagDescription.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetApiTagDescription(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apiTagDescriptions()
            .getWithResponse(
                "rg1", "apimService1", "59d6bb8f1f7fab13dc67ec9b", "59306a29e4bbd510dc24e5f9", Context.NONE);
    }
}
```
