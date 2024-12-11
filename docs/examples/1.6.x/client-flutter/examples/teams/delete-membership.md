import 'package:appwrite/appwrite.dart';

Client client = Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('<YOUR_PROJECT_ID>'); // Your project ID

Teams teams = Teams(client);

await teams.deleteMembership(
    teamId: '<TEAM_ID>',
    membershipId: '<MEMBERSHIP_ID>',
);