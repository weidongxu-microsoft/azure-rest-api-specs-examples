Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.management.serializer.SerializerFactory;
import com.azure.core.util.Context;
import com.azure.core.util.serializer.SerializerEncoding;
import java.io.IOException;

/** Samples for Snapshots Update. */
public final class Main {
    /*
     * operationId: Snapshots_Update
     * api-version: 2021-06-01
     * x-ms-examples: Snapshots_Update
     */
    /**
     * Sample code: Snapshots_Update.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void snapshotsUpdate(com.azure.resourcemanager.netapp.NetAppFilesManager manager) throws IOException {
        manager
            .snapshots()
            .update(
                "myRG",
                "account1",
                "pool1",
                "volume1",
                "snapshot1",
                SerializerFactory
                    .createDefaultManagementSerializerAdapter()
                    .deserialize("{}", Object.class, SerializerEncoding.JSON),
                Context.NONE);
    }
}
```
