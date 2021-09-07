Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Subscription Delete. */
public final class Main {
    /*
     * operationId: Subscription_Delete
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementDeleteSubscription
     */
    /**
     * Sample code: ApiManagementDeleteSubscription.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementDeleteSubscription(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.subscriptions().deleteWithResponse("rg1", "apimService1", "testsub", "*", Context.NONE);
    }
}
```
