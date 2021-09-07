Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.netapp.models.CheckNameResourceTypes;
import com.azure.resourcemanager.netapp.models.ResourceNameAvailabilityRequest;

/** Samples for NetAppResource CheckNameAvailability. */
public final class Main {
    /*
     * operationId: NetAppResource_CheckNameAvailability
     * api-version: 2021-06-01
     * x-ms-examples: CheckNameAvailability
     */
    /**
     * Sample code: CheckNameAvailability.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void checkNameAvailability(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager
            .netAppResources()
            .checkNameAvailabilityWithResponse(
                "eastus",
                new ResourceNameAvailabilityRequest()
                    .withName("accName")
                    .withType(CheckNameResourceTypes.fromString("netAppAccount"))
                    .withResourceGroup("myRG"),
                Context.NONE);
    }
}
```
