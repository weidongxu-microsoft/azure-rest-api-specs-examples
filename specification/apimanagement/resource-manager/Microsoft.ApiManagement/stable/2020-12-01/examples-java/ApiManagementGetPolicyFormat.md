Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.PolicyExportFormat;
import com.azure.resourcemanager.apimanagement.models.PolicyIdName;

/** Samples for Policy Get. */
public final class Main {
    /*
     * operationId: Policy_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetPolicyFormat
     */
    /**
     * Sample code: ApiManagementGetPolicyFormat.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetPolicyFormat(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .policies()
            .getWithResponse("rg1", "apimService1", PolicyIdName.POLICY, PolicyExportFormat.RAWXML, Context.NONE);
    }
}
```
