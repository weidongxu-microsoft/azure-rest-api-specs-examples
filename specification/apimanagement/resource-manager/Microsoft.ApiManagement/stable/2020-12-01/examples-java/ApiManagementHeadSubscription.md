Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Subscription GetEntityTag. */
public final class Main {
    /*
     * operationId: Subscription_GetEntityTag
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementHeadSubscription
     */
    /**
     * Sample code: ApiManagementHeadSubscription.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementHeadSubscription(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .subscriptions()
            .getEntityTagWithResponse("rg1", "apimService1", "5931a769d8d14f0ad8ce13b8", Context.NONE);
    }
}
```
