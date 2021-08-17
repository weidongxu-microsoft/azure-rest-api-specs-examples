```java
import com.azure.core.util.Context;

/** Samples for Operations List. */
public final class OperationsList {
    /*
     * operationId: Operations_List
     * api-version: 2018-06-01
     * x-ms-examples: Operations_List
     */
    /**
     * Sample code: Operations_List.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void operationsList(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.operations().list(Context.NONE);
    }
}
```