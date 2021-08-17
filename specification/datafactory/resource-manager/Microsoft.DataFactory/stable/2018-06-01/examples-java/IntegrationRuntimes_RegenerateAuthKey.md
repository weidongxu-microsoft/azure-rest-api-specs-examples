```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.IntegrationRuntimeAuthKeyName;
import com.azure.resourcemanager.datafactory.models.IntegrationRuntimeRegenerateKeyParameters;

/** Samples for IntegrationRuntimes RegenerateAuthKey. */
public final class IntegrationRuntimesRegenerateAuthKey {
    /*
     * operationId: IntegrationRuntimes_RegenerateAuthKey
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_RegenerateAuthKey
     */
    /**
     * Sample code: IntegrationRuntimes_RegenerateAuthKey.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesRegenerateAuthKey(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimes()
            .regenerateAuthKeyWithResponse(
                "exampleResourceGroup",
                "exampleFactoryName",
                "exampleIntegrationRuntime",
                new IntegrationRuntimeRegenerateKeyParameters().withKeyName(IntegrationRuntimeAuthKeyName.AUTH_KEY2),
                Context.NONE);
    }
}
```