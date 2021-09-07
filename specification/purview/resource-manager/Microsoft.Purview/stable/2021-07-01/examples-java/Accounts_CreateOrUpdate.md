Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-purview_1.0.0-beta.1/sdk/purview/azure-resourcemanager-purview/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.resourcemanager.purview.models.AccountSku;
import com.azure.resourcemanager.purview.models.Name;

/** Samples for Accounts CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Accounts_CreateOrUpdate
     * api-version: 2021-07-01
     * x-ms-examples: Accounts_CreateOrUpdate
     */
    /**
     * Sample code: Accounts_CreateOrUpdate.
     *
     * @param manager Entry point to PurviewManager.
     */
    public static void accountsCreateOrUpdate(com.azure.resourcemanager.purview.PurviewManager manager) {
        manager
            .accounts()
            .define("account1")
            .withRegion("West US 2")
            .withExistingResourceGroup("SampleResourceGroup")
            .withSku(new AccountSku().withCapacity(4).withName(Name.STANDARD))
            .withManagedResourceGroupName("custom-rgname")
            .create();
    }
}
```
