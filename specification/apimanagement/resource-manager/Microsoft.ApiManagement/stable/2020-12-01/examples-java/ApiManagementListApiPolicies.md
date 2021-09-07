Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for ApiPolicy ListByApi. */
public final class Main {
    /*
     * operationId: ApiPolicy_ListByApi
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListApiPolicies
     */
    /**
     * Sample code: ApiManagementListApiPolicies.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListApiPolicies(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apiPolicies().listByApiWithResponse("rg1", "apimService1", "5600b59475ff190048040001", Context.NONE);
    }
}
```
