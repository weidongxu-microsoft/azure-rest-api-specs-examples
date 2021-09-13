Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.NotificationName;

/** Samples for NotificationRecipientEmail CheckEntityExists. */
public final class Main {
    /*
     * operationId: NotificationRecipientEmail_CheckEntityExists
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementHeadNotificationRecipientEmail
     */
    /**
     * Sample code: ApiManagementHeadNotificationRecipientEmail.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementHeadNotificationRecipientEmail(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .notificationRecipientEmails()
            .checkEntityExistsWithResponse(
                "rg1",
                "apimService1",
                NotificationName.REQUEST_PUBLISHER_NOTIFICATION_MESSAGE,
                "contoso@live.com",
                Context.NONE);
    }
}
```
