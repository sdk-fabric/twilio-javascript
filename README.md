
# twilio-javascript

This [SDK](https://github.com/sdk-fabric/twilio-javascript) is managed by the [SDK Fabric](https://sdk-fabric.org/) project, a global infrastructure to
automatically generate SDKs for every API.

You can find more information about this SDK at [TypeHub](https://typehub.cloud/):
https://app.typehub.cloud/d/sdkfabric/twilio

## Usage

```typescript
const client = Client::build('[access_token]');

// Delete the Media resource.
const response = await client.media().delete("accountSid", "messageSid", "sid");

// Fetch a single Media resource associated with a specific Message resource.
const response = await client.media().get("accountSid", "messageSid", "sid");

// Read a list of Media resources associated with a specific Message resource.
const response = await client.media().getAll("DateCreated", 1, 1, "PageToken", "accountSid", "messageSid");

// Send a message (SMS, MMS, WhatsApp or other channel).
const response = await client.messages().create("accountSid", new any());

// Deletes a Message resource from your account.
const response = await client.messages().delete("accountSid", "sid");

// Fetch a specific Message.
const response = await client.messages().get("accountSid", "sid");

// Retrieve a list of Message resources associated with a Twilio Account.
const response = await client.messages().getAll("DateSent", "From", 1, 1, "PageToken", "To", "accountSid");

// Update a Message resource (used to redact Message `body` text and to cancel not-yet-sent messages).
const response = await client.messages().update("accountSid", "sid", new any());
```
