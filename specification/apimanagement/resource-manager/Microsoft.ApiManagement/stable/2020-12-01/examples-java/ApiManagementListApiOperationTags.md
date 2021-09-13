Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Tag ListByOperation. */
public final class Main {
    /*
     * operationId: Tag_ListByOperation
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListApiOperationTags
     */
    /**
     * Sample code: ApiManagementListApiOperationTags.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListApiOperationTags(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .tags()
            .listByOperation(
                "rg1",
                "apimService1",
                "57d2ef278aa04f0888cba3f3",
                "57d2ef278aa04f0888cba3f6",
                null,
                null,
                null,
                Context.NONE);
    }
}
```
