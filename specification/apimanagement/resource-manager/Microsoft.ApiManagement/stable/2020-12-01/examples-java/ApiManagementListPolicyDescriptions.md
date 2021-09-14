Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.PolicyScopeContract;

/** Samples for PolicyDescription ListByService. */
public final class Main {
    /*
     * operationId: PolicyDescription_ListByService
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListPolicyDescriptions
     */
    /**
     * Sample code: ApiManagementListPolicyDescriptions.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListPolicyDescriptions(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .policyDescriptions()
            .listByServiceWithResponse("rg1", "apimService1", PolicyScopeContract.API, Context.NONE);
    }
}
```
