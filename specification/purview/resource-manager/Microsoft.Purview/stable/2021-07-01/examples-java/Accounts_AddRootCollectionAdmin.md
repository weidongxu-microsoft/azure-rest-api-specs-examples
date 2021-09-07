Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-purview_1.0.0-beta.1/sdk/purview/azure-resourcemanager-purview/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.purview.models.CollectionAdminUpdate;

/** Samples for Accounts AddRootCollectionAdmin. */
public final class Main {
    /*
     * operationId: Accounts_AddRootCollectionAdmin
     * api-version: 2021-07-01
     * x-ms-examples: Accounts_AddRootCollectionAdmin
     */
    /**
     * Sample code: Accounts_AddRootCollectionAdmin.
     *
     * @param manager Entry point to PurviewManager.
     */
    public static void accountsAddRootCollectionAdmin(com.azure.resourcemanager.purview.PurviewManager manager) {
        manager
            .accounts()
            .addRootCollectionAdminWithResponse(
                "SampleResourceGroup",
                "account1",
                new CollectionAdminUpdate().withObjectId("7e8de0e7-2bfc-4e1f-9659-2a5785e4356f"),
                Context.NONE);
    }
}
```
