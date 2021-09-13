Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
/** Samples for Tag CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Tag_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateTag
     */
    /**
     * Sample code: ApiManagementCreateTag.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateTag(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.tags().define("tagId1").withExistingService("rg1", "apimService1").withDisplayName("tag1").create();
    }
}
```
