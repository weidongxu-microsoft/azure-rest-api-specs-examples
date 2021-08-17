```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.ExposureControlRequest;

/** Samples for ExposureControl GetFeatureValueByFactory. */
public final class ExposureControlGetFeatureValueByFactory {
    /*
     * operationId: ExposureControl_GetFeatureValueByFactory
     * api-version: 2018-06-01
     * x-ms-examples: ExposureControl_GetFeatureValueByFactory
     */
    /**
     * Sample code: ExposureControl_GetFeatureValueByFactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void exposureControlGetFeatureValueByFactory(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .exposureControls()
            .getFeatureValueByFactoryWithResponse(
                "exampleResourceGroup",
                "exampleFactoryName",
                new ExposureControlRequest()
                    .withFeatureName("ADFIntegrationRuntimeSharingRbac")
                    .withFeatureType("Feature"),
                Context.NONE);
    }
}
```