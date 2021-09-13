Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-postgresqlflexibleserver_1.0.0-beta.3/sdk/postgresqlflexibleserver/azure-resourcemanager-postgresqlflexibleserver/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.postgresqlflexibleserver.models.Backup;
import com.azure.resourcemanager.postgresqlflexibleserver.models.CreateModeForUpdate;
import com.azure.resourcemanager.postgresqlflexibleserver.models.MaintenanceWindow;
import com.azure.resourcemanager.postgresqlflexibleserver.models.Server;
import com.azure.resourcemanager.postgresqlflexibleserver.models.Sku;
import com.azure.resourcemanager.postgresqlflexibleserver.models.SkuTier;
import com.azure.resourcemanager.postgresqlflexibleserver.models.Storage;

/** Samples for Servers Update. */
public final class Main {
    /*
     * operationId: Servers_Update
     * api-version: 2021-06-01
     * x-ms-examples: ServerUpdateWithCustomerMaintenanceWindow
     */
    /**
     * Sample code: ServerUpdateWithCustomerMaintenanceWindow.
     *
     * @param manager Entry point to PostgreSqlManager.
     */
    public static void serverUpdateWithCustomerMaintenanceWindow(
        com.azure.resourcemanager.postgresqlflexibleserver.PostgreSqlManager manager) {
        Server resource =
            manager.servers().getByResourceGroupWithResponse("testrg", "pgtestsvc4", Context.NONE).getValue();
        resource
            .update()
            .withMaintenanceWindow(
                new MaintenanceWindow()
                    .withCustomWindow("Enabled")
                    .withStartHour(8)
                    .withStartMinute(0)
                    .withDayOfWeek(0))
            .withCreateMode(CreateModeForUpdate.UPDATE)
            .apply();
    }
}
```