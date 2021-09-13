Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
/** Samples for Certificate CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Certificate_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateCertificate
     */
    /**
     * Sample code: ApiManagementCreateCertificate.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateCertificate(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .certificates()
            .define("tempcert")
            .withExistingService("rg1", "apimService1")
            .withData("****************Base 64 Encoded Certificate *******************************")
            .withPassword("****Certificate Password******")
            .create();
    }
}
```
