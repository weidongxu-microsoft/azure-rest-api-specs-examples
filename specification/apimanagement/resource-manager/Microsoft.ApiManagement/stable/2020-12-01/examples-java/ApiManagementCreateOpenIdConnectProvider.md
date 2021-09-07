Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

/** Samples for OpenIdConnectProvider CreateOrUpdate. */
public final class Main {
    /*
     * operationId: OpenIdConnectProvider_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateOpenIdConnectProvider
     */
    /**
     * Sample code: ApiManagementCreateOpenIdConnectProvider.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateOpenIdConnectProvider(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .openIdConnectProviders()
            .define("templateOpenIdConnect3")
            .withExistingService("rg1", "apimService1")
            .withDisplayName("templateoidprovider3")
            .withMetadataEndpoint("https://oidprovider-template3.net")
            .withClientId("oidprovidertemplate3")
            .withClientSecret("x")
            .create();
    }
}
```
