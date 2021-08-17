```java
import com.azure.core.util.Context;

/** Samples for Datasets ListByFactory. */
public final class DatasetsListByFactory {
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