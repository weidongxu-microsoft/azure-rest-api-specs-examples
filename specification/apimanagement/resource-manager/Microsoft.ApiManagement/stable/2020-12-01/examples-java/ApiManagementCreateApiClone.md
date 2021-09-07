Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.resourcemanager.apimanagement.models.ApiCreateOrUpdatePropertiesWsdlSelector;
import com.azure.resourcemanager.apimanagement.models.AuthenticationSettingsContract;
import com.azure.resourcemanager.apimanagement.models.BearerTokenSendingMethods;
import com.azure.resourcemanager.apimanagement.models.ContentFormat;
import com.azure.resourcemanager.apimanagement.models.OAuth2AuthenticationSettingsContract;
import com.azure.resourcemanager.apimanagement.models.OpenIdAuthenticationSettingsContract;
import com.azure.resourcemanager.apimanagement.models.Protocol;
import com.azure.resourcemanager.apimanagement.models.SoapApiType;
import com.azure.resourcemanager.apimanagement.models.SubscriptionKeyParameterNamesContract;
import java.util.Arrays;

/** Samples for Api CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Api_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateApiClone
     */
    /**
     * Sample code: ApiManagementCreateApiClone.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateApiClone(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apis()
            .define("echo-api2")
            .withExistingService("rg1", "apimService1")
            .withSourceApiId(
                "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.ApiManagement/service/apimService1/apis/58a4aeac497000007d040001")
            .withDisplayName("Echo API2")
            .withServiceUrl("http://echoapi.cloudapp.net/api")
            .withPath("echo2")
            .withProtocols(Arrays.asList(Protocol.HTTP, Protocol.HTTPS))
            .withDescription("Copy of Existing Echo Api including Operations.")
            .withIsCurrent(true)
            .withSubscriptionRequired(true)
            .create();
    }
}
```
