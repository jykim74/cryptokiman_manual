# CryptokiMan Features by License Status

CryptokiMan checks for a valid license at startup. The comparison below describes the application controls in the current source. Actual operations also depend on the loaded PKCS #11 module, token capabilities, and token permissions.

## Feature comparison

| Feature | Valid license | No valid license |
|---|---|---|
| Load a PKCS #11 module; view slots, tokens, sessions, and object information | Available | Available |
| Open and close sessions; log in and log out | Available | Available |
| Initialize or finalize the PKCS #11 module | Available | Available |
| Initialize a token; initialize or change its PIN | Available | Unavailable |
| Generate random data and run digest operations | Available | Unavailable |
| Sign, verify, encrypt, and decrypt | Available | Unavailable |
| Create key objects, edit attributes, delete or copy objects | Available | Unavailable |
| Import certificates, PFX files, and private keys | Available | Unavailable |
| Export keys or certificates; view key material | Available | Unavailable |
| Wrap, unwrap, or derive keys | Available | Unavailable |
| Create a certificate signing request (CSR) | Available | Unavailable |
| HSM management and CAVP tools | Available | Unavailable |
| View application logs | Available | Unavailable |

Without a valid license, CryptokiMan remains useful for loading a module, inspecting available token and object information, and managing sessions. License-restricted controls are disabled in the interface. Some operation dialogs also restrict input modes or algorithms; the exact behavior depends on the operation.

## Getting a license

The application includes a license information dialog for requesting or importing a license. The project guide also provides a [free trial license request](https://jykim7.mycafe24.com/user_reg.php). Restart CryptokiMan after changing the license to apply it.

## Notes

- An expired, invalid, or mismatched license is treated as unlicensed.
- A license enables application features; it does not add capabilities that the PKCS #11 module or token does not support.
- “Available” means the application permits the action. The token may still reject it because of its mechanism support, object attributes, login state, or policy.
