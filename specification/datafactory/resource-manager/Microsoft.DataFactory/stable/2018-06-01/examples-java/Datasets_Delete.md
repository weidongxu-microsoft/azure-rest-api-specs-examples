```java
import com.azure.core.util.Context;

/** Samples for Datasets Delete. */
public final class DatasetsDelete {
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