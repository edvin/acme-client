# Java ACME Client

This fork makes the ACME Client compatible with the Wildfly Application Server.

For some reason, the HttpClient that comes with Wildfly barfs at some of the response from Let's Encrypt.

This is circumvented by returning an instance of JerseyRestClient instead of using the ClientBuilder.newClient() functionality to create the client, as that would fall back to the client included with Wildfly.