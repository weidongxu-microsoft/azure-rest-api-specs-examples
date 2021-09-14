Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.fluent.models.PortalDelegationSettingsInner;
import com.azure.resourcemanager.apimanagement.models.RegistrationDelegationSettingsProperties;
import com.azure.resourcemanager.apimanagement.models.SubscriptionsDelegationSettingsProperties;

/** Samples for DelegationSettings CreateOrUpdate. */
public final class Main {
    /*
     * operationId: DelegationSettings_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementPortalSettingsUpdateDelegation
     */
    /**
     * Sample code: ApiManagementPortalSettingsUpdateDelegation.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementPortalSettingsUpdateDelegation(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .delegationSettings()
            .createOrUpdateWithResponse(
                "rg1",
                "apimService1",
                new PortalDelegationSettingsInner()
                    .withUrl("http://contoso.com/delegation")
                    .withValidationKey("<validationKey>")
                    .withSubscriptions(new SubscriptionsDelegationSettingsProperties().withEnabled(true))
                    .withUserRegistration(new RegistrationDelegationSettingsProperties().withEnabled(true)),
                "*",
                Context.NONE);
    }
}
```
