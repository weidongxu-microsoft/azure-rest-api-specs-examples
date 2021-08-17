```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.GitHubAccessTokenRequest;

/** Samples for Factories GetGitHubAccessToken. */
public final class FactoriesGetGitHubAccessToken {
    /*
     * operationId: Factories_GetGitHubAccessToken
     * api-version: 2018-06-01
     * x-ms-examples: Factories_GetGitHubAccessToken
     */
    /**
     * Sample code: Factories_GetGitHubAccessToken.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void factoriesGetGitHubAccessToken(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .factories()
            .getGitHubAccessTokenWithResponse(
                "exampleResourceGroup",
                "exampleFactoryName",
                new GitHubAccessTokenRequest()
                    .withGitHubAccessCode("some")
                    .withGitHubClientId("some")
                    .withGitHubAccessTokenBaseUrl("some"),
                Context.NONE);
    }
}
```