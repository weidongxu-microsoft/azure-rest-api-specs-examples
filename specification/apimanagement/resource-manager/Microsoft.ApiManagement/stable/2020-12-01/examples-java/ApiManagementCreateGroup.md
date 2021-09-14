Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
/** Samples for Group CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Group_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateGroup
     */
    /**
     * Sample code: ApiManagementCreateGroup.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateGroup(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .groups()
            .define("tempgroup")
            .withExistingService("rg1", "apimService1")
            .withDisplayName("temp group")
            .create();
    }
}
```
