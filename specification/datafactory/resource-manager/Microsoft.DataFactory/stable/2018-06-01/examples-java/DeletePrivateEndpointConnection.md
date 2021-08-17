```java
import com.azure.core.util.Context;

/** Samples for PrivateEndpointConnectionOperation Delete. */
public final class DeletePrivateEndpointConnection {
    /*
     * operationId: PrivateEndpointConnection_Delete
     * api-version: 2018-06-01
     * x-ms-examples: Delete a private endpoint connection for a datafactory.
     */
    /**
     * Sample code: Delete a private endpoint connection for a datafactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void deleteAPrivateEndpointConnectionForADatafactory(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .privateEndpointConnectionOperations()
            .deleteWithResponse("exampleResourceGroup", "exampleFactoryName", "connection", Context.NONE);
    }
}
```