Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.fluent.models.PolicyContractInner;
import com.azure.resourcemanager.apimanagement.models.PolicyContentFormat;
import com.azure.resourcemanager.apimanagement.models.PolicyIdName;

/** Samples for Policy CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Policy_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreatePolicy
     */
    /**
     * Sample code: ApiManagementCreatePolicy.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreatePolicy(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .policies()
            .createOrUpdateWithResponse(
                "rg1",
                "apimService1",
                PolicyIdName.POLICY,
                new PolicyContractInner()
                    .withValue(
                        "<policies>\r\n"
                            + "  <inbound />\r\n"
                            + "  <backend>\r\n"
                            + "    <forward-request />\r\n"
                            + "  </backend>\r\n"
                            + "  <outbound />\r\n"
                            + "</policies>")
                    .withFormat(PolicyContentFormat.XML),
                null,
                Context.NONE);
    }
}
```
