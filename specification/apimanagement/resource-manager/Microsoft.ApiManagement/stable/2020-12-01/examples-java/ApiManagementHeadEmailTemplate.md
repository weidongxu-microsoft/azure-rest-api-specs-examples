Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.TemplateName;

/** Samples for EmailTemplate GetEntityTag. */
public final class Main {
    /*
     * operationId: EmailTemplate_GetEntityTag
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementHeadEmailTemplate
     */
    /**
     * Sample code: ApiManagementHeadEmailTemplate.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementHeadEmailTemplate(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .emailTemplates()
            .getEntityTagWithResponse("rg1", "apimService1", TemplateName.NEW_ISSUE_NOTIFICATION_MESSAGE, Context.NONE);
    }
}
```
