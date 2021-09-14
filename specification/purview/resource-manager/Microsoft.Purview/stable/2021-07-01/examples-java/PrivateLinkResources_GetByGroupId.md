Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-purview_1.0.0-beta.1/sdk/purview/azure-resourcemanager-purview/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for PrivateLinkResources GetByGroupId. */
public final class Main {
    /*
     * operationId: PrivateLinkResources_GetByGroupId
     * api-version: 2021-07-01
     * x-ms-examples: PrivateLinkResources_GetByGroupId
     */
    /**
     * Sample code: PrivateLinkResources_GetByGroupId.
     *
     * @param manager Entry point to PurviewManager.
     */
    public static void privateLinkResourcesGetByGroupId(com.azure.resourcemanager.purview.PurviewManager manager) {
        manager
            .privateLinkResources()
            .getByGroupIdWithResponse("SampleResourceGroup", "account1", "group1", Context.NONE);
    }
}
```
