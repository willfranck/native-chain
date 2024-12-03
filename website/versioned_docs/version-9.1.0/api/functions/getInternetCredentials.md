# Function: getInternetCredentials()

> **getInternetCredentials**(`server`, `options`?): `Promise`\<`false` \| [`UserCredentials`](../type-aliases/UserCredentials.md)\>

Fetches the internet credentials for the given server.

## Parameters

• **server**: `string`

The server URL.

• **options?**: [`GetOptions`](../type-aliases/GetOptions.md)

A keychain options object.

## Returns

`Promise`\<`false` \| [`UserCredentials`](../type-aliases/UserCredentials.md)\>

Resolves to an object containing `server`, `username`, `password`, and `storage` when successful, or `false` on failure.

## Example

```typescript
const credentials = await Keychain.getInternetCredentials('https://example.com');
if (credentials) {
  console.log('Credentials loaded for user ' + credentials.username);
} else {
  console.log('No credentials stored for server');
}
```

## Defined in

[index.ts:202](https://github.com/oblador/react-native-keychain/blob/7eaf30e4858d9a03afd4c8e017b83a96fbc4e982/src/index.ts#L202)