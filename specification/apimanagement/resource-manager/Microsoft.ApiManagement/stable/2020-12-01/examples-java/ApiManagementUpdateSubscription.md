Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.SubscriptionUpdateParameters;

/** Samples for Subscription Update. */
public final class Main {
    /*
     * operationId: Subscription_Update
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementUpdateSubscription
     */
    /**
     * Sample code: ApiManagementUpdateSubscription.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementUpdateSubscription(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .subscriptions()
            .updateWithResponse(
                "rg1",
                "apimService1",
                "testsub",
                "*",
                new SubscriptionUpdateParameters().withDisplayName("testsub"),
                null,
                null,
                Context.NONE);
    }
}
```
