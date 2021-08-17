```java
import com.azure.resourcemanager.datafactory.models.PrivateLinkConnectionApprovalRequest;
import com.azure.resourcemanager.datafactory.models.PrivateLinkConnectionState;

/** Samples for PrivateEndpointConnectionOperation CreateOrUpdate. */
public final
class ApproveRejectPrivateEndpointConnection {
    /*
     * operationId: PrivateEndpointConnection_CreateOrUpdate
     * api-version: 2018-06-01
     * x-ms-examples: Approves or rejects a private endpoint connection for a factory.
     */
    /**
     * Sample code: Approves or rejects a private endpoint connection for a factory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void approvesOrRejectsAPrivateEndpointConnectionForAFactory(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .privateEndpointConnectionOperations()
            .define("connection")
            .withExistingFactory("exampleResourceGroup", "exampleFactoryName")
            .withProperties(
                new PrivateLinkConnectionApprovalRequest()
                    .withPrivateLinkServiceConnectionState(
                        new PrivateLinkConnectionState()
                            .withStatus("Approved")
                            .withDescription("Approved by admin.")
                            .withActionsRequired("")))
            .create();
    }
}
```