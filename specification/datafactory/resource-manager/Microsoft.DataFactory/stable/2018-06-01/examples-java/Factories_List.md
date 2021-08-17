```java
import com.azure.core.util.Context;

/** Samples for Factories List. */
public final class FactoriesList {
    /*
     * operationId: Factories_List
     * api-version: 2018-06-01
     * x-ms-examples: Factories_List
     */
    /**
     * Sample code: Factories_List.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void factoriesList(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.factories().list(Context.NONE);
    }
}
```