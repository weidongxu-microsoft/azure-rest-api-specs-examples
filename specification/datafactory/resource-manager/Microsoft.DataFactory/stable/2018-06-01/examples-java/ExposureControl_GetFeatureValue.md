Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.ExposureControlRequest;

/** Samples for ExposureControl GetFeatureValue. */
public final class Main {
    /*
     * operationId: ExposureControl_GetFeatureValue
     * api-version: 2018-06-01
     * x-ms-examples: ExposureControl_GetFeatureValue
     */
    /**
     * Sample code: ExposureControl_GetFeatureValue.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void exposureControlGetFeatureValue(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .exposureControls()
            .getFeatureValueWithResponse(
                "WestEurope",
                new ExposureControlRequest()
                    .withFeatureName("ADFIntegrationRuntimeSharingRbac")
                    .withFeatureType("Feature"),
                Context.NONE);
    }
}
```
