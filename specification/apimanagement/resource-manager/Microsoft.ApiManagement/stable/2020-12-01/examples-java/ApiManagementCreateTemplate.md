Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.resourcemanager.apimanagement.models.TemplateName;

/** Samples for EmailTemplate CreateOrUpdate. */
public final class Main {
    /*
     * operationId: EmailTemplate_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateTemplate
     */
    /**
     * Sample code: ApiManagementCreateTemplate.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateTemplate(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .emailTemplates()
            .define(TemplateName.NEW_ISSUE_NOTIFICATION_MESSAGE)
            .withExistingService("rg1", "apimService1")
            .withSubject("Your request for $IssueName was successfully received.")
            .create();
    }
}
```
