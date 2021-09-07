Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-purview_1.0.0-beta.1/sdk/purview/azure-resourcemanager-purview/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.purview.models.ScopeType;
import java.util.UUID;

/** Samples for DefaultAccounts Get. */
public final class Main {
    /*
     * operationId: DefaultAccounts_Get
     * api-version: 2021-07-01
     * x-ms-examples: DefaultAccounts_Get
     */
    /**
     * Sample code: DefaultAccounts_Get.
     *
     * @param manager Entry point to PurviewManager.
     */
    public static void defaultAccountsGet(com.azure.resourcemanager.purview.PurviewManager manager) {
        manager
            .defaultAccounts()
            .getWithResponse(
                UUID.fromString("12345678-1234-1234-12345678abc"),
                ScopeType.TENANT,
                "12345678-1234-1234-12345678abc",
                Context.NONE);
    }
}
```
