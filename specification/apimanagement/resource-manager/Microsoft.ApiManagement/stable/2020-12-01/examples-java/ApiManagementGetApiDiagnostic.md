Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for ApiDiagnostic Get. */
public final class Main {
    /*
     * operationId: ApiDiagnostic_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetApiDiagnostic
     */
    /**
     * Sample code: ApiManagementGetApiDiagnostic.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetApiDiagnostic(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apiDiagnostics()
            .getWithResponse("rg1", "apimService1", "57d1f7558aa04f15146d9d8a", "applicationinsights", Context.NONE);
    }
}
```
