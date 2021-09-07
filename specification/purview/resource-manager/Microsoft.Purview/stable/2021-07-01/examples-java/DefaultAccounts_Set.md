Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-purview_1.0.0-beta.1/sdk/purview/azure-resourcemanager-purview/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.purview.fluent.models.DefaultAccountPayloadInner;
import com.azure.resourcemanager.purview.models.ScopeType;

/** Samples for DefaultAccounts Set. */
public final class Main {
    /*
     * operationId: DefaultAccounts_Set
     * api-version: 2021-07-01
     * x-ms-examples: DefaultAccounts_Set
     */
    /**
     * Sample code: DefaultAccounts_Set.
     *
     * @param manager Entry point to PurviewManager.
     */
    public static void defaultAccountsSet(com.azure.resourcemanager.purview.PurviewManager manager) {
        manager
            .defaultAccounts()
            .setWithResponse(
                new DefaultAccountPayloadInner()
                    .withAccountName("myDefaultAccount")
                    .withResourceGroupName("rg-1")
                    .withScope("12345678-1234-1234-12345678abc")
                    .withScopeTenantId("12345678-1234-1234-12345678abc")
                    .withScopeType(ScopeType.TENANT)
                    .withSubscriptionId("12345678-1234-1234-12345678aaa"),
                Context.NONE);
    }
}
```
