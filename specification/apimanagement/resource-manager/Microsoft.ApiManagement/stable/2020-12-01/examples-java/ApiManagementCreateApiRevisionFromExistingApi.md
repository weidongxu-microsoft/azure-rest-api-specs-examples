Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
/** Samples for Api CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Api_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateApiRevisionFromExistingApi
     */
    /**
     * Sample code: ApiManagementCreateApiRevisionFromExistingApi.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateApiRevisionFromExistingApi(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apis()
            .define("echo-api;rev=3")
            .withExistingService("rg1", "apimService1")
            .withSourceApiId(
                "/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.ApiManagement/service/apimService1/apis/echo-api")
            .withServiceUrl("http://echoapi.cloudapp.net/apiv3")
            .withPath("echo")
            .withApiRevisionDescription("Creating a Revision of an existing API")
            .create();
    }
}
```
