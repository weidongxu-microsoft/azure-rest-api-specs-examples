```java
import com.azure.core.util.Context;

/** Samples for PrivateEndpointConnectionOperation Get. */
public final class GetPrivateEndpointConnection {
    /*
     * operationId: PrivateEndpointConnection_Get
     * api-version: 2018-06-01
     * x-ms-examples: Get a private endpoint connection for a datafactory.
     */
    /**
     * Sample code: Get a private endpoint connection for a datafactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void getAPrivateEndpointConnectionForADatafactory(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .privateEndpointConnectionOperations()
            .getWithResponse("exampleResourceGroup", "exampleFactoryName", "connection", null, Context.NONE);
    }
}
```