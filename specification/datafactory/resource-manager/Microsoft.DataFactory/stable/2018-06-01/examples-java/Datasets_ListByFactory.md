Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Datasets ListByFactory. */
public final class Main {
    /*
     * operationId: Datasets_ListByFactory
     * api-version: 2018-06-01
     * x-ms-examples: Datasets_ListByFactory
     */
    /**
     * Sample code: Datasets_ListByFactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void datasetsListByFactory(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.datasets().listByFactory("exampleResourceGroup", "exampleFactoryName", Context.NONE);
    }
}
```
