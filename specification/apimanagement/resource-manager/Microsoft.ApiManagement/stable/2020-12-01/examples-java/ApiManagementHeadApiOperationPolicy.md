Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.PolicyIdName;

/** Samples for ApiOperationPolicy GetEntityTag. */
public final class Main {
    /*
     * operationId: ApiOperationPolicy_GetEntityTag
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementHeadApiOperationPolicy
     */
    /**
     * Sample code: ApiManagementHeadApiOperationPolicy.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementHeadApiOperationPolicy(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apiOperationPolicies()
            .getEntityTagWithResponse(
                "rg1",
                "apimService1",
                "5600b539c53f5b0062040001",
                "5600b53ac53f5b0062080006",
                PolicyIdName.POLICY,
                Context.NONE);
    }
}
```
