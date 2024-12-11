import io.appwrite.Client;
import io.appwrite.coroutines.CoroutineCallback;
import io.appwrite.services.Teams;

Client client = new Client()
    .setEndpoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .setProject("<YOUR_PROJECT_ID>") // Your project ID
    .setSession(""); // The user session to authenticate with

Teams teams = new Teams(client);

teams.create(
    "<TEAM_ID>", // teamId
    "<NAME>", // name
    listOf(), // roles (optional)
    new CoroutineCallback<>((result, error) -> {
        if (error != null) {
            error.printStackTrace();
            return;
        }

        System.out.println(result);
    })
);
