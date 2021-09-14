Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
/** Samples for GatewayCertificateAuthority CreateOrUpdate. */
public final class Main {
    /*
     * operationId: GatewayCertificateAuthority_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateGatewayCertificateAuthority
     */
    /**
     * Sample code: ApiManagementCreateGatewayCertificateAuthority.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateGatewayCertificateAuthority(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .gatewayCertificateAuthorities()
            .define("cert1")
            .withExistingGateway("rg1", "apimService1", "gw1")
            .withIsTrusted(false)
            .create();
    }
}
```
