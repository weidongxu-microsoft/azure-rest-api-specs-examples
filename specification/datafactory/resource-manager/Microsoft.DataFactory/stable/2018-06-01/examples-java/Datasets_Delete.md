Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Datasets Delete. */
public final class Main {
    /*
     * operationId: Datasets_Delete
     * api-version: 2018-06-01
     * x-ms-examples: Datasets_Delete
     */
    /**
     * Sample code: Datasets_Delete.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void datasetsDelete(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .datasets()
            .deleteWithResponse("exampleResourceGroup", "exampleFactoryName", "exampleDataset", Context.NONE);
    }
}
```
