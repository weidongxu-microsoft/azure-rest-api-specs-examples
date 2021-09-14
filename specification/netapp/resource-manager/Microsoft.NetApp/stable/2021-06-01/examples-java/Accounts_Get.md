Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Accounts GetByResourceGroup. */
public final class Main {
    /*
     * operationId: Accounts_Get
     * api-version: 2021-06-01
     * x-ms-examples: Accounts_Get
     */
    /**
     * Sample code: Accounts_Get.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void accountsGet(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager.accounts().getByResourceGroupWithResponse("myRG", "account1", Context.NONE);
    }
}
```
