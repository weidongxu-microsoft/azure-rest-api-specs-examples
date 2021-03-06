Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-synapse_1.0.0-beta.4/sdk/synapse/azure-resourcemanager-synapse/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.synapse.models.SecurityAlertPolicyNameAutoGenerated;
import com.azure.resourcemanager.synapse.models.SecurityAlertPolicyState;
import com.azure.resourcemanager.synapse.models.ServerSecurityAlertPolicy;

/** Samples for WorkspaceManagedSqlServerSecurityAlertPolicy CreateOrUpdate. */
public final class Main {
    /*
     * x-ms-original-file: specification/synapse/resource-manager/Microsoft.Synapse/stable/2021-06-01/examples/WorkspaceManagedSqlServerSecurityAlertCreateWithMinParameters.json
     */
    /**
     * Sample code: Update a workspace managed sql server's threat detection policy with minimal parameters.
     *
     * @param manager Entry point to SynapseManager.
     */
    public static void updateAWorkspaceManagedSqlServerSThreatDetectionPolicyWithMinimalParameters(
        com.azure.resourcemanager.synapse.SynapseManager manager) {
        ServerSecurityAlertPolicy resource =
            manager
                .workspaceManagedSqlServerSecurityAlertPolicies()
                .getWithResponse(
                    "wsg-7398", "testWorkspace", SecurityAlertPolicyNameAutoGenerated.DEFAULT, Context.NONE)
                .getValue();
        resource
            .update()
            .withState(SecurityAlertPolicyState.DISABLED)
            .withEmailAccountAdmins(true)
            .withStorageEndpoint("https://mystorage.blob.core.windows.net")
            .withStorageAccountAccessKey(
                "sdlfkjabc+sdlfkjsdlkfsjdfLDKFTERLKFDFKLjsdfksjdflsdkfD2342309432849328476458/3RSD==")
            .apply();
    }
}
```
