Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for NetworkStatus ListByLocation. */
public final class Main {
    /*
     * operationId: NetworkStatus_ListByLocation
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementServiceGetNetworkStatusByLocation
     */
    /**
     * Sample code: ApiManagementServiceGetNetworkStatusByLocation.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementServiceGetNetworkStatusByLocation(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.networkStatus().listByLocationWithResponse("rg1", "apimService1", "North Central US", Context.NONE);
    }
}
```
