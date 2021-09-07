Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-purview_1.0.0-beta.1/sdk/purview/azure-resourcemanager-purview/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Accounts List. */
public final class Main {
    /*
     * operationId: Accounts_ListBySubscription
     * api-version: 2021-07-01
     * x-ms-examples: Accounts_ListBySubscription
     */
    /**
     * Sample code: Accounts_ListBySubscription.
     *
     * @param manager Entry point to PurviewManager.
     */
    public static void accountsListBySubscription(com.azure.resourcemanager.purview.PurviewManager manager) {
        manager.accounts().list(null, Context.NONE);
    }
}
```
