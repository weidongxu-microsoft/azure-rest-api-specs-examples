Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.ApiManagementServiceCheckNameAvailabilityParameters;

/** Samples for ApiManagementService CheckNameAvailability. */
public final class Main {
    /*
     * operationId: ApiManagementService_CheckNameAvailability
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementServiceCheckNameAvailability
     */
    /**
     * Sample code: ApiManagementServiceCheckNameAvailability.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementServiceCheckNameAvailability(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apiManagementServices()
            .checkNameAvailabilityWithResponse(
                new ApiManagementServiceCheckNameAvailabilityParameters().withName("apimService1"), Context.NONE);
    }
}
```
