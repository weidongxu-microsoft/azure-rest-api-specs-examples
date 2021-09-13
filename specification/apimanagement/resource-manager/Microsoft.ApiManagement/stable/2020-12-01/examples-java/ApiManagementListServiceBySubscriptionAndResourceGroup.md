Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ApiManagementService ListByResourceGroup. */
public final class Main {
    /*
     * operationId: ApiManagementService_ListByResourceGroup
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListServiceBySubscriptionAndResourceGroup
     */
    /**
     * Sample code: ApiManagementListServiceBySubscriptionAndResourceGroup.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListServiceBySubscriptionAndResourceGroup(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apiManagementServices().listByResourceGroup("rg1", Context.NONE);
    }
}
```
