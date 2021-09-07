Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Api Get. */
public final class Main {
    /*
     * operationId: Api_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetApiRevisionContract
     */
    /**
     * Sample code: ApiManagementGetApiRevisionContract.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetApiRevisionContract(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apis().getWithResponse("rg1", "apimService1", "echo-api;rev=3", Context.NONE);
    }
}
```
