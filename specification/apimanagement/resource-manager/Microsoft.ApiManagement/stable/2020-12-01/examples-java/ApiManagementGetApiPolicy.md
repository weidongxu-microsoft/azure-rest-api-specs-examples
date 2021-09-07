Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.PolicyIdName;

/** Samples for ApiPolicy Get. */
public final class Main {
    /*
     * operationId: ApiPolicy_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetApiPolicy
     */
    /**
     * Sample code: ApiManagementGetApiPolicy.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetApiPolicy(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apiPolicies()
            .getWithResponse(
                "rg1", "apimService1", "5600b59475ff190048040001", PolicyIdName.POLICY, null, Context.NONE);
    }
}
```
