```java
import com.azure.core.util.Context;

/** Samples for Factories GetByResourceGroup. */
public final class FactoriesGet {
    /*
     * operationId: Factories_Get
     * api-version: 2018-06-01
     * x-ms-examples: Factories_Get
     */
    /**
     * Sample code: Factories_Get.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void factoriesGet(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .factories()
            .getByResourceGroupWithResponse("exampleResourceGroup", "exampleFactoryName", null, Context.NONE);
    }
}
```