Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.UserContract;

/** Samples for User Update. */
public final class Main {
    /*
     * operationId: User_Update
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementUpdateUser
     */
    /**
     * Sample code: ApiManagementUpdateUser.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementUpdateUser(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        UserContract resource =
            manager.users().getWithResponse("rg1", "apimService1", "5931a75ae4bbd512a88c680b", Context.NONE).getValue();
        resource
            .update()
            .withEmail("foobar@outlook.com")
            .withFirstName("foo")
            .withLastName("bar")
            .withIfMatch("*")
            .apply();
    }
}
```
