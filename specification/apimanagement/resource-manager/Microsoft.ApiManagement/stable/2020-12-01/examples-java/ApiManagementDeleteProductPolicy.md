Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.PolicyIdName;

/** Samples for ProductPolicy Delete. */
public final class Main {
    /*
     * operationId: ProductPolicy_Delete
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementDeleteProductPolicy
     */
    /**
     * Sample code: ApiManagementDeleteProductPolicy.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementDeleteProductPolicy(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .productPolicies()
            .deleteWithResponse("rg1", "apimService1", "testproduct", PolicyIdName.POLICY, "*", Context.NONE);
    }
}
```
