Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-purview_1.0.0-beta.1/sdk/purview/azure-resourcemanager-purview/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for PrivateLinkResources ListByAccount. */
public final class Main {
    /*
     * operationId: PrivateLinkResources_ListByAccount
     * api-version: 2021-07-01
     * x-ms-examples: PrivateLinkResources_ListByAccount
     */
    /**
     * Sample code: PrivateLinkResources_ListByAccount.
     *
     * @param manager Entry point to PurviewManager.
     */
    public static void privateLinkResourcesListByAccount(com.azure.resourcemanager.purview.PurviewManager manager) {
        manager.privateLinkResources().listByAccount("SampleResourceGroup", "account1", Context.NONE);
    }
}
```
