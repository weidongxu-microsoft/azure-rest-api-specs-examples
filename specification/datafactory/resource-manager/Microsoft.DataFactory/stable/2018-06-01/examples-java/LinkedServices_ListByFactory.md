```java
import com.azure.core.util.Context;

/** Samples for LinkedServices ListByFactory. */
public final class LinkedServicesListByFactory {
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