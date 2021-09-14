Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for LinkedServices ListByFactory. */
public final class Main {
    /*
     * operationId: LinkedServices_ListByFactory
     * api-version: 2018-06-01
     * x-ms-examples: LinkedServices_ListByFactory
     */
    /**
     * Sample code: LinkedServices_ListByFactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void linkedServicesListByFactory(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.linkedServices().listByFactory("exampleResourceGroup", "exampleFactoryName", Context.NONE);
    }
}
```
