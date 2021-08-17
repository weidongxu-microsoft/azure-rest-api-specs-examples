```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.CreateDataFlowDebugSessionRequest;
import com.azure.resourcemanager.datafactory.models.DataFlowComputeType;
import com.azure.resourcemanager.datafactory.models.IntegrationRuntimeComputeProperties;
import com.azure.resourcemanager.datafactory.models.IntegrationRuntimeDataFlowProperties;
import com.azure.resourcemanager.datafactory.models.IntegrationRuntimeDebugResource;
import com.azure.resourcemanager.datafactory.models.ManagedIntegrationRuntime;

/** Samples for DataFlowDebugSession Create. */
public final class DataFlowDebugSessionCreate {
    /*
     * operationId: DataFlowDebugSession_Create
     * api-version: 2018-06-01
     * x-ms-examples: DataFlowDebugSession_Create
     */
    /**
     * Sample code: DataFlowDebugSession_Create.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void dataFlowDebugSessionCreate(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .dataFlowDebugSessions()
            .create(
                "exampleResourceGroup",
                "exampleFactoryName",
                new CreateDataFlowDebugSessionRequest()
                    .withTimeToLive(60)
                    .withIntegrationRuntime(
                        new IntegrationRuntimeDebugResource()
                            .withName("ir1")
                            .withProperties(
                                new ManagedIntegrationRuntime()
                                    .withComputeProperties(
                                        new IntegrationRuntimeComputeProperties()
                                            .withLocation("AutoResolve")
                                            .withDataFlowProperties(
                                                new IntegrationRuntimeDataFlowProperties()
                                                    .withComputeType(DataFlowComputeType.GENERAL)
                                                    .withCoreCount(48)
                                                    .withTimeToLive(10))))),
                Context.NONE);
    }
}
```