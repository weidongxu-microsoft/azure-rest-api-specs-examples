Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.ExposureControlBatchRequest;
import com.azure.resourcemanager.datafactory.models.ExposureControlRequest;
import java.util.Arrays;

/** Samples for ExposureControl QueryFeatureValuesByFactory. */
public final class Main {
    /*
     * operationId: ExposureControl_QueryFeatureValuesByFactory
     * api-version: 2018-06-01
     * x-ms-examples: ExposureControl_QueryFeatureValuesByFactory
     */
    /**
     * Sample code: ExposureControl_QueryFeatureValuesByFactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void exposureControlQueryFeatureValuesByFactory(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .exposureControls()
            .queryFeatureValuesByFactoryWithResponse(
                "exampleResourceGroup",
                "exampleFactoryName",
                new ExposureControlBatchRequest()
                    .withExposureControlRequests(
                        Arrays
                            .asList(
                                new ExposureControlRequest()
                                    .withFeatureName("ADFIntegrationRuntimeSharingRbac")
                                    .withFeatureType("Feature"),
                                new ExposureControlRequest()
                                    .withFeatureName("ADFSampleFeature")
                                    .withFeatureType("Feature"))),
                Context.NONE);
    }
}
```
