Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.NotificationName;

/** Samples for Notification Get. */
public final class Main {
    /*
     * operationId: Notification_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetNotification
     */
    /**
     * Sample code: ApiManagementGetNotification.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetNotification(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .notifications()
            .getWithResponse(
                "rg1", "apimService1", NotificationName.REQUEST_PUBLISHER_NOTIFICATION_MESSAGE, Context.NONE);
    }
}
```
