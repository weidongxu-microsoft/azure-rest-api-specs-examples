Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Subscription List. */
public final class Main {
    /*
     * operationId: Subscription_List
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListSubscriptions
     */
    /**
     * Sample code: ApiManagementListSubscriptions.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListSubscriptions(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.subscriptions().list("rg1", "apimService1", null, null, null, Context.NONE);
    }
}
```
