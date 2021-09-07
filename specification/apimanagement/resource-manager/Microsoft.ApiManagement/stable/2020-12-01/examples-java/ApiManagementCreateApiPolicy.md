Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.fluent.models.PolicyContractInner;
import com.azure.resourcemanager.apimanagement.models.PolicyContentFormat;
import com.azure.resourcemanager.apimanagement.models.PolicyIdName;

/** Samples for ApiPolicy CreateOrUpdate. */
public final class Main {
    /*
     * operationId: ApiPolicy_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateApiPolicy
     */
    /**
     * Sample code: ApiManagementCreateApiPolicy.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateApiPolicy(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apiPolicies()
            .createOrUpdateWithResponse(
                "rg1",
                "apimService1",
                "5600b57e7e8880006a040001",
                PolicyIdName.POLICY,
                new PolicyContractInner()
                    .withValue(
                        "<policies> <inbound /> <backend>    <forward-request />  </backend>  <outbound /></policies>")
                    .withFormat(PolicyContentFormat.XML),
                "*",
                Context.NONE);
    }
}
```
