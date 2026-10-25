# CryptokiMan Basic Usage

CryptokiMan is a graphical utility for working with PKCS #11 (Cryptoki) modules. It can inspect a module, its slots and tokens, and—subject to the token's capabilities and your license—manage sessions and objects or run cryptographic operations.

## Before you start

1. Install the vendor's PKCS #11 module and any required device drivers.
2. Identify the module library file for your operating system and application architecture. For example, a 64-bit application requires a 64-bit module.
3. Make sure the token or HSM is available. For a software test environment, SoftHSM can provide a PKCS #11 module without hardware.
4. Have the appropriate User PIN or Security Officer (SO) PIN available if the operation requires authentication.

> CryptokiMan communicates with the device through the PKCS #11 library you load. Available mechanisms, operations, and object permissions are determined by that module and token.

## Load a PKCS #11 module

1. Start CryptokiMan.
2. Select **File > Open...** and choose the PKCS #11 library file. You can also drag the library file into the main window.
3. Wait for the module to initialize. The navigation tree should show the library and its slots.
4. Select a slot or token to inspect its information and supported mechanisms in the details and information areas.

Only one Cryptoki module can be loaded at a time. Close active sessions and unload the current module before loading another one.

## Open a session and log in

1. Select the slot or token you want to use.
2. Choose **Module > Open Session**.
3. Choose read-only access for inspection. Choose read/write access only when you need to create, change, or remove objects and the token permits it.
4. To perform an operation that requires authentication, choose the login command and select the correct role:
   - **User** for normal token operations.
   - **Security Officer (SO)** for administrative tasks supported by the token.
5. Enter the PIN assigned to that role.

Do not confuse the User PIN with the SO PIN. The token may restrict or reject operations based on the role, session type, or login state.

## Browse objects

After opening a session, browse the object categories in the navigation tree. Select an object or row to view its available information. Double-click or right-click an object to see the actions supported for it, such as viewing details or managing attributes.

Object visibility and editable attributes depend on the token's policy. Sensitive key values may not be readable or exportable, even when the object itself is listed.

## Run an operation

CryptokiMan provides dialogs for supported operations such as random data generation, digesting, signing and verification, and encryption and decryption. A typical operation is:

1. Open the relevant command from the **Cryptography** menu or toolbar.
2. Select a mechanism supported by the module.
3. Select the required key or object, if the operation uses one.
4. Enter the data or choose an input file, and set any required parameters.
5. Run the operation and review the result and status messages.

For signing, decryption, or other private-key operations, the selected key must permit the requested action and the token may require an authenticated session. If an operation fails, check the selected mechanism, key attributes, session state, and the **Information** and **Log** panels.

## Close and unload

1. Log out when you no longer need the authenticated session.
2. Close the session using **Module > Close Session** (or the corresponding session command). Close all sessions before unloading the module.
3. Unload or close the loaded module from the **Module** menu before exiting or loading another library.

## Important cautions

- **Initialize Token** replaces the token's initialization state and can erase existing token data. Use it only when you intend to initialize that token.
- PIN initialization and changes affect access to the token. Follow the device vendor's recovery and PIN policies.
- A read/write session permits changes only when the token and the authenticated role allow them.
- Some CryptokiMan features require a valid license. A license does not add mechanisms or permissions that the module or token does not support.

## Try with SoftHSM

SoftHSM is a software implementation of a PKCS #11 token and can be used for development and testing. Configure SoftHSM and initialize a test token using its own documentation and utilities, then load the SoftHSM library in CryptokiMan and follow the steps above. Keep test tokens separate from production credentials and data.

## Related documentation

- [CryptokiMan overview and downloads](CRYPTOKIMAN_EN.md)
- [Features by license status](LICENSE_FEATURES.md)
- [CryptokiMan manual articles](https://jykim74.tistory.com/category/Manual/CryptokiMan)
- [Original CryptokiMan introduction](https://jykim74.tistory.com/38)
- [SoftHSM usage on Windows and Linux](https://jykim74.tistory.com/140)
