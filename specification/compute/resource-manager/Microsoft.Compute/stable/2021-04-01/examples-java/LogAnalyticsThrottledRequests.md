```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.ThrottledRequestsInput;
import java.time.OffsetDateTime;

/** Samples for LogAnalytics ExportThrottledRequests. */
public final
class LogAnalyticsThrottledRequests {
    /*
     * operationId: LogAnalytics_ExportThrottledRequests
     * api-version: 2021-04-01
     * x-ms-examples: Export logs which contain all throttled Api requests made to Compute Resource Provider within the given time period.
     */
    /**
     * Sample code: Export logs which contain all throttled Api requests made to Compute Resource Provider within the
     * given time period.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void
        exportLogsWhichContainAllThrottledApiRequestsMadeToComputeResourceProviderWithinTheGivenTimePeriod(
            com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getLogAnalytics()
            .exportThrottledRequests(
                "westus",
                new ThrottledRequestsInput()
                    .withBlobContainerSasUri("https://somesasuri")
                    .withFromTime(OffsetDateTime.parse("2018-01-21T01:54:06.862601Z"))
                    .withToTime(OffsetDateTime.parse("2018-01-23T01:54:06.862601Z"))
                    .withGroupByOperationName(true)
                    .withGroupByResourceName(false)
                    .withGroupByClientApplicationId(false)
                    .withGroupByUserAgent(false),
                Context.NONE);
    }
}
```