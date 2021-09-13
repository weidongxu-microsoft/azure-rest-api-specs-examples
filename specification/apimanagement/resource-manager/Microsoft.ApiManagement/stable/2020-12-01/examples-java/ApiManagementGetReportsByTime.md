Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import java.time.Duration;

/** Samples for Reports ListByTime. */
public final class Main {
    /*
     * operationId: Reports_ListByTime
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetReportsByTime
     */
    /**
     * Sample code: ApiManagementGetReportsByTime.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetReportsByTime(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .reports()
            .listByTime(
                "rg1",
                "apimService1",
                "timestamp ge datetime'2017-06-01T00:00:00' and timestamp le datetime'2017-06-04T00:00:00'",
                Duration.parse("PT15M"),
                null,
                null,
                null,
                Context.NONE);
    }
}
```
