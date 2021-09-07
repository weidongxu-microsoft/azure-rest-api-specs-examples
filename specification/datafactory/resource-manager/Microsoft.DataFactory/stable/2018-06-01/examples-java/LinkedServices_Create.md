Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.management.serializer.SerializerFactory;
import com.azure.core.util.Context;
import com.azure.core.util.serializer.SerializerEncoding;
import com.azure.resourcemanager.datafactory.models.AzureStorageLinkedService;
import com.azure.resourcemanager.datafactory.models.LinkedServiceResource;
import java.io.IOException;

/** Samples for LinkedServices CreateOrUpdate. */
public final class Main {
    /*
     * operationId: LinkedServices_CreateOrUpdate
     * api-version: 2018-06-01
     * x-ms-examples: LinkedServices_Create
     */
    /**
     * Sample code: LinkedServices_Create.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void linkedServicesCreate(com.azure.resourcemanager.datafactory.DataFactoryManager manager)
        throws IOException {
        manager
            .linkedServices()
            .define("exampleLinkedService")
            .withExistingFactory("exampleResourceGroup", "exampleFactoryName")
            .withProperties(
                new AzureStorageLinkedService()
                    .withConnectionString(
                        SerializerFactory
                            .createDefaultManagementSerializerAdapter()
                            .deserialize(
                                "{\"type\":\"SecureString\",\"value\":\"DefaultEndpointsProtocol=https;AccountName=examplestorageaccount;AccountKey=<storage"
                                    + " key>\"}",
                                Object.class,
                                SerializerEncoding.JSON)))
            .create();
    }
}
```