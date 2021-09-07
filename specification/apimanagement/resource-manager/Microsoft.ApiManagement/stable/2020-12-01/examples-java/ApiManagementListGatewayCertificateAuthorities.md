Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for GatewayCertificateAuthority ListByService. */
public final class Main {
    /*
     * operationId: GatewayCertificateAuthority_ListByService
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListGatewaycertificateAuthorities
     */
    /**
     * Sample code: ApiManagementListGatewaycertificateAuthorities.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListGatewaycertificateAuthorities(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .gatewayCertificateAuthorities()
            .listByService("rg1", "apimService1", "gw1", null, null, null, Context.NONE);
    }
}
```
