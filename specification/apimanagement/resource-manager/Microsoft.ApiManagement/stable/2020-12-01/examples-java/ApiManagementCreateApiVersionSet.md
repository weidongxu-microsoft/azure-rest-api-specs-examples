Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.resourcemanager.apimanagement.models.VersioningScheme;

/** Samples for ApiVersionSet CreateOrUpdate. */
public final class Main {
    /*
     * operationId: ApiVersionSet_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateApiVersionSet
     */
    /**
     * Sample code: ApiManagementCreateApiVersionSet.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateApiVersionSet(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apiVersionSets()
            .define("api1")
            .withExistingService("rg1", "apimService1")
            .withDisplayName("api set 1")
            .withVersioningScheme(VersioningScheme.SEGMENT)
            .withDescription("Version configuration")
            .create();
    }
}
```
