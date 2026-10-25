# CryptokiMan Menu Guide

This guide summarizes CryptokiMan's menus and the actions they provide for tokens, sessions, objects, and cryptographic operations.

## File

| Command | Description |
|---|---|
| **New** | Opens another CryptokiMan window. |
| **Open...** | Selects and loads a Cryptoki library. Only one library can be loaded at a time. |
| **Unload** | Unloads the currently loaded Cryptoki library. |
| **Show log tab** | Shows the Information and Log dock at the bottom of the window. |
| **Recent Files** | Opens a previously loaded library. The menu keeps up to ten recent entries. |
| **Quit** | Exits CryptokiMan. |

## View

The **View** menu is available when the application has a valid license. Its submenus contain checkable options for showing or hiding individual buttons on the File, Module, Object, Cryptogram, Import, Tools, and Help toolbars. The Cryptogram toolbar contains the **Cryptography** menu commands. Changing a toolbar option does not remove the command from its main menu.

## Module

| Command | Description |
|---|---|
| **Initialize** | Initializes the PKCS #11 library (`C_Initialize`). |
| **Finalize** | Finalizes the PKCS #11 library (`C_Finalize`). |
| **Open Session** | Opens a session on the selected token (`C_OpenSession`). |
| **Close Session** | Closes the selected session (`C_CloseSession`). |
| **Close All Sessions** | Closes all sessions for the selected token (`C_CloseAllSessions`). |
| **Login** | Logs in to the selected session, for example as a user or security officer (`C_Login`). |
| **Logout** | Logs out of the selected session (`C_Logout`). |

## Objects

| Command | Description |
|---|---|
| **Generate Key Pair** | Generates a public/private key pair on the token (`C_GenerateKeyPair`). |
| **Generate Key** | Generates a secret key on the token (`C_GenerateKey`). |
| **Create Data** | Creates a data object using the supplied attributes (`C_CreateObject`). |
| **Create RSA Public Key** | Creates an RSA public-key object from supplied attributes. |
| **Create RSA Private Key** | Creates an RSA private-key object from supplied attributes. |
| **Create ECDSA Public Key** | Creates an elliptic-curve public-key object, commonly used for ECDSA. |
| **Create ECDSA Private Key** | Creates an elliptic-curve private-key object, commonly used for ECDSA. |
| **Create EDDSA Public Key** | Creates an Edwards-curve digital-signature public-key object. |
| **Create EDDSA Private Key** | Creates an Edwards-curve digital-signature private-key object. |
| **Create DSA Public Key** | Creates a DSA public-key object from supplied attributes. |
| **Create DSA Private Key** | Creates a DSA private-key object from supplied attributes. |
| **Create PQC Public Key** | Creates a post-quantum cryptography public-key object supported by the library. |
| **Create PQC Private Key** | Creates a post-quantum cryptography private-key object supported by the library. |
| **Create Key** | Creates a key object from a supplied template. |
| **Destroy Object** | Destroys the selected token object (`C_DestroyObject`). |
| **Edit Object** | Edits attributes of the selected object. Whether an attribute can be changed depends on the token. |
| **Edit Attribute List** | Edits a list of attributes for the selected object. |
| **Copy Object** | Copies the selected object, optionally with changed attributes (`C_CopyObject`). |
| **Find Objects** | Searches the selected session for objects matching supplied attributes. |

## Cryptography

| Command | Description |
|---|---|
| **Random** | Generates random bytes using the token (`C_GenerateRandom`). |
| **Digest** | Computes a message digest using a supported mechanism. |
| **Signature** | Signs data using a selected private key and signature mechanism. |
| **Verify** | Verifies a signature using data, a signature, and a suitable public key. |
| **Encrypt** | Encrypts data using a selected key and supported mechanism. |
| **Decrypt** | Decrypts data using a selected key and supported mechanism. |
| **HSM Manage** | Opens the HSM management window. Available management operations depend on the configured HSM. |

## Import

| Command | Description |
|---|---|
| **Import certificate** | Imports a certificate and creates a certificate object on the token. |
| **Import PFX** | Imports a PKCS #12/PFX file. The file may contain certificates and a private key. |
| **Import Private Key** | Imports a supported private-key file and creates a key object on the token. |

## Tools

| Command | Description |
|---|---|
| **Initialize Token** | Initializes the selected token (`C_InitToken`), including its label and security-officer PIN. Token initialization may erase existing token data. |
| **Operation State** | Reads or restores the state of an operation when supported by the token. |
| **Set PIN** | Changes a token PIN (`C_SetPIN`). |
| **Init PIN** | Initializes the user PIN (`C_InitPIN`), generally after security-officer authentication. |
| **Wrap Key** | Wraps (exports in encrypted form) a key using a wrapping key and supported mechanism. |
| **Unwrap Key** | Unwraps a key and creates a corresponding key object on the token. |
| **Derive Key** | Derives a new key from a base key using a supported mechanism. |
| **Type Name** | Opens the type-name utility for PKCS #11 type information. |
| **Make CSR** | Creates a certificate signing request (CSR) using a key and request details. |
| **CAVP** | Opens the Cryptographic Algorithm Validation Program utility. |

## Help

| Command | Description |
|---|---|
| **Clear Log** | Clears the messages in the Log tab. This command is created when a valid license is present. |
| **Log** | Toggles logging. The command's status tip says “Halt log”; it is created when a valid license is present. |
| **Settings** | Opens CryptokiMan settings. |
| **License Information** | Displays license information. |
| **Bug or Issue Report** | Opens the project's bug or issue reporting page. |
| **Q and A** | Opens the project's Q&A or discussion page. |
| **About CryptokiMan** | Displays information about the application. |

## Object table context menu

Right-click an object row to show commands for that object type. The menu is not shown for the root, slot, token, mechanism, or session tree items.

| Command | Description |
|---|---|
| **View Object** | Displays details of the selected object. |
| **Edit Attribute** | Edits an attribute of the selected object. |
| **Edit AttributeList** | Opens the attribute-list editor. |
| **Delete Object** | Destroys the selected object. |
| **View Certificate** | Displays certificate details. Shown for certificate objects. |
| **Export Certficate** | Exports a certificate object. Shown for certificate objects. |
| **Verify / Encrypt** | Uses a public key for signature verification or encryption. Shown for public-key objects. |
| **Export PublicKey / View PublicKey** | Exports or displays a public key. |
| **Sign / Decrypt** | Uses a private key to sign or decrypt. Shown for private-key objects. |
| **Export PrivateKey / View PrivateKey** | Exports or displays a private key, subject to token permissions. |
| **Make CSR** | Creates a CSR using a private-key object. |
| **Sign / Verify / Encrypt / Decrypt** | Offers supported cryptographic operations for a secret-key object. |
| **Copy Object** | Copies the selected object. Available for certificate, public-key, private-key, secret-key, and data objects. |

Commands may be disabled when the license does not enable the operation. Actual success also depends on the PKCS #11 module, token, session state, key attributes, and mechanism support.
