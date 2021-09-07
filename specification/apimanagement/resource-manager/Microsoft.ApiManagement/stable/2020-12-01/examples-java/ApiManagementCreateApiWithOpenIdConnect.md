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
     * x-ms-examples: ApiManagementCreateApiWithOpenIdConnect
     */
    /**
     * Sample code: ApiManagementCreateApiWithOpenIdConnect.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateApiWithOpenIdConnect(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apis()
            .define("tempgroup")
            .withExistingService("rg1", "apimService1")
            .withDisplayName("Swagger Petstore")
            .withServiceUrl("http://petstore.swagger.io/v2")
            .withPath("petstore")
            .withProtocols(Arrays.asList(Protocol.HTTPS))
            .withDescription(
                "This is a sample server Petstore server.  You can find out more about Swagger at"
                    + " [http://swagger.io](http://swagger.io) or on [irc.freenode.net,"
                    + " #swagger](http://swagger.io/irc/).  For this sample, you can use the api key `special-key` to"
                    + " test the authorization filters.")
            .withAuthenticationSettings(
                new AuthenticationSettingsContract()
                    .withOpenid(
                        new OpenIdAuthenticationSettingsContract()
                            .withOpenidProviderId("testopenid")
                            .withBearerTokenSendingMethods(
                                Arrays.asList(BearerTokenSendingMethods.AUTHORIZATION_HEADER))))
            .withSubscriptionKeyParameterNames(
                new SubscriptionKeyParameterNamesContract()
                    .withHeaderProperty("Ocp-Apim-Subscription-Key")
                    .withQuery("subscription-key"))
            .create();
    }
}
```
