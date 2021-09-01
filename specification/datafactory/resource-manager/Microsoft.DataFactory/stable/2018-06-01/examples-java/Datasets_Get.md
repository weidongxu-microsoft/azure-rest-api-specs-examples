Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Datasets Get. */
public final class Main {
    /*
     * operationId: Datasets_Get
     * api-version: 2018-06-01
     * x-ms-examples: Datasets_Get
     */
    /**
     * Sample code: Datasets_Get.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void datasetsGet(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .datasets()
            .getWithResponse("exampleResourceGroup", "exampleFactoryName", "exampleDataset", null, Context.NONE);
    }
}
```
