Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Issue Get. */
public final class Main {
    /*
     * operationId: Issue_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetIssue
     */
    /**
     * Sample code: ApiManagementGetIssue.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetIssue(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.issues().getWithResponse("rg1", "apimService1", "57d2ef278aa04f0ad01d6cdc", Context.NONE);
    }
}
```
