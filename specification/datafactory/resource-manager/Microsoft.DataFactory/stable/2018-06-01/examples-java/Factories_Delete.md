```java
import com.azure.core.util.Context;

/** Samples for Factories Delete. */
public final class FactoriesDelete {
    /*
     * operationId: Factories_Delete
     * api-version: 2018-06-01
     * x-ms-examples: Factories_Delete
     */
    /**
     * Sample code: Factories_Delete.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void factoriesDelete(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.factories().deleteWithResponse("exampleResourceGroup", "exampleFactoryName", Context.NONE);
    }
}
```