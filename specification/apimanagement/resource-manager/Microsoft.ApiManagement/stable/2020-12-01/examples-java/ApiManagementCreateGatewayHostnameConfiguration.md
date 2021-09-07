Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

/** Samples for GatewayHostnameConfiguration CreateOrUpdate. */
public final class Main {
    /*
     * operationId: GatewayHostnameConfiguration_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateGatewayHostnameConfiguration
     */
    /**
     * Sample code: ApiManagementCreateGatewayHostnameConfiguration.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateGatewayHostnameConfiguration(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .gatewayHostnameConfigurations()
            .define("default")
            .withExistingGateway("rg1", "apimService1", "gw1")
            .withHostname("*")
            .withCertificateId(
                "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.ApiManagement/service/apimService1/certificates/cert1")
            .withNegotiateClientCertificate(false)
            .withTls10Enabled(false)
            .withTls11Enabled(false)
            .withHttp2Enabled(true)
            .create();
    }
}
```
