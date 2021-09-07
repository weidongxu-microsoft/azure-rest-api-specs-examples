Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-purview_1.0.0-beta.1/sdk/purview/azure-resourcemanager-purview/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.purview.models.CheckNameAvailabilityRequest;

/** Samples for Accounts CheckNameAvailability. */
public final class Main {
    /*
     * operationId: Accounts_CheckNameAvailability
     * api-version: 2021-07-01
     * x-ms-examples: Accounts_CheckNameAvailability
     */
    /**
     * Sample code: Accounts_CheckNameAvailability.
     *
     * @param manager Entry point to PurviewManager.
     */
    public static void accountsCheckNameAvailability(com.azure.resourcemanager.purview.PurviewManager manager) {
        manager
            .accounts()
            .checkNameAvailabilityWithResponse(
                new CheckNameAvailabilityRequest().withName("account1").withType("Microsoft.Purview/accounts"),
                Context.NONE);
    }
}
```
