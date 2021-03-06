Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager_2.10.0/sdk/resourcemanager/azure-resourcemanager/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.containerregistry.fluent.models.ImportPipelineInner;
import com.azure.resourcemanager.containerregistry.models.IdentityProperties;
import com.azure.resourcemanager.containerregistry.models.ImportPipelineSourceProperties;
import com.azure.resourcemanager.containerregistry.models.PipelineOptions;
import com.azure.resourcemanager.containerregistry.models.PipelineSourceType;
import com.azure.resourcemanager.containerregistry.models.ResourceIdentityType;
import com.azure.resourcemanager.containerregistry.models.UserIdentityProperties;
import java.util.Arrays;
import java.util.HashMap;
import java.util.Map;

/** Samples for ImportPipelines Create. */
public final class Main {
    /*
     * x-ms-original-file: specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/examples/ImportPipelineCreate.json
     */
    /**
     * Sample code: ImportPipelineCreate.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void importPipelineCreate(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .containerRegistries()
            .manager()
            .serviceClient()
            .getImportPipelines()
            .create(
                "myResourceGroup",
                "myRegistry",
                "myImportPipeline",
                new ImportPipelineInner()
                    .withLocation("westus")
                    .withIdentity(
                        new IdentityProperties()
                            .withType(ResourceIdentityType.USER_ASSIGNED)
                            .withUserAssignedIdentities(
                                mapOf(
                                    "/subscriptions/f9d7ebed-adbd-4cb4-b973-aaf82c136138/resourcegroups/myResourceGroup/providers/Microsoft.ManagedIdentity/userAssignedIdentities/identity2",
                                    new UserIdentityProperties())))
                    .withSource(
                        new ImportPipelineSourceProperties()
                            .withType(PipelineSourceType.AZURE_STORAGE_BLOB_CONTAINER)
                            .withUri("https://accountname.blob.core.windows.net/containername")
                            .withKeyVaultUri("https://myvault.vault.azure.net/secrets/acrimportsas"))
                    .withOptions(
                        Arrays
                            .asList(
                                PipelineOptions.OVERWRITE_TAGS,
                                PipelineOptions.DELETE_SOURCE_BLOB_ON_SUCCESS,
                                PipelineOptions.CONTINUE_ON_ERRORS)),
                Context.NONE);
    }

    @SuppressWarnings("unchecked")
    private static <T> Map<String, T> mapOf(Object... inputs) {
        Map<String, T> map = new HashMap<>();
        for (int i = 0; i < inputs.length; i += 2) {
            String key = (String) inputs[i];
            T value = (T) inputs[i + 1];
            map.put(key, value);
        }
        return map;
    }
}
```
