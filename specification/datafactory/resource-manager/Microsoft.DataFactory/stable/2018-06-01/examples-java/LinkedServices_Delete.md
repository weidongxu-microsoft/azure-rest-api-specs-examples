```java
import com.azure.core.util.Context;

/** Samples for LinkedServices Delete. */
public final class LinkedServicesDelete {
    /*
     * operationId: LinkedServices_Delete
     * api-version: 2018-06-01
     * x-ms-examples: LinkedServices_Delete
     */
    /**
     * Sample code: LinkedServices_Delete.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void linkedServicesDelete(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .linkedServices()
            .deleteWithResponse("exampleResourceGroup", "exampleFactoryName", "exampleLinkedService", Context.NONE);
    }
}
```