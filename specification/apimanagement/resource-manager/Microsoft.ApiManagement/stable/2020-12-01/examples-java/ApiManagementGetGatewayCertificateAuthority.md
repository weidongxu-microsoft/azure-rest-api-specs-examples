Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for GatewayCertificateAuthority Get. */
public final class Main {
    /*
     * operationId: GatewayCertificateAuthority_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetGatewayCertificateAuthority
     */
    /**
     * Sample code: ApiManagementGetGatewayCertificateAuthority.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetGatewayCertificateAuthority(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.gatewayCertificateAuthorities().getWithResponse("rg1", "apimService1", "gw1", "cert1", Context.NONE);
    }
}
```
