# CryptokiMan Menu Guide

This guide summarizes CryptokiMan's menus and the actions they provide for tokens, sessions, objects, and cryptographic operations.

## File

| Command | Description |
|---|---|
| **New** | Opens another CryptokiMan window. |
| **Open...** | Selects and loads a PKCS #11 Cryptoki library. The library provides access to the cryptographic token or HSM. |
| **Unload** | Unloads the currently loaded Cryptoki library. |
| **Show log tab** | Shows the information and log dock at the bottom of the window. |
| **Recent Files** | Reopens one of the recently loaded Cryptoki libraries. |
| **Quit** | Exits CryptokiMan. |

## View

The **View** menu configures which actions appear on each toolbar. Its submenus are **File ToolBar**, **Module ToolBar**, **Object ToolBar**, **Cryptogram ToolBar**, **Import ToolBar**, **Tools ToolBar**, and **Help ToolBar**. Each submenu contains checkable items corresponding to the commands in the matching menu; checking an item shows that command on the toolbar, and unchecking it hides the toolbar button. The command remains available from its main menu.

## Module

These commands operate on the loaded PKCS #11 module, its slots, and sessions.

| Command | Description |
|---|---|
| **Initialize** | Initializes the Cryptoki module (`C_Initialize`) before using its services. |
| **Finalize** | Finalizes the Cryptoki module (`C_Finalize`) and releases module state. |
| **Open Session** | Opens a session on the selected token (`C_OpenSession`). |
| **Close Session** | Closes the selected session (`C_CloseSession`). |
| **Close All Sessions** | Closes all sessions for the selected token (`C_CloseAllSessions`). |
| **Login** | Authenticates to the token in the selected session (`C_Login`), typically as a user or security officer. |
| **Logout** | Ends the current authenticated state for the selected session (`C_Logout`). |

## Objects

Create, inspect, find, copy, edit, or destroy objects in the selected session. Availability depends on token support and object permissions.

| Command | Description |
|---|---|
| **Generate Key Pair** | Generates a public/private key pair on the token (`C_GenerateKeyPair`). |
| **Generate Key** | Generates a secret key on the token (`C_GenerateKey`). |
| **Create Data** | Creates a data object with the supplied attributes (`C_CreateObject`). |
| **Create RSA Public Key** | Creates an RSA public-key object from the supplied key attributes. |
| **Create RSA Private Key** | Creates an RSA private-key object from the supplied key attributes. |
| **Create ECDSA Public Key** | Creates an elliptic-curve public-key object (commonly used for ECDSA). |
| **Create ECDSA Private Key** | Creates an elliptic-curve private-key object (commonly used for ECDSA). |
| **Create EDDSA Public Key** | Creates an Edwards-curve digital-signature public-key object. |
| **Create EDDSA Private Key** | Creates an Edwards-curve digital-signature private-key object. |
| **Create DSA Public Key** | Creates a DSA public-key object from the supplied key attributes. |
| **Create DSA Private Key** | Creates a DSA private-key object from the supplied key attributes. |
| **Create PQC Public Key** | Creates a post-quantum cryptography public-key object supported by the module. |
| **Create PQC Private Key** | Creates a post-quantum cryptography private-key object supported by the module. |
| **Create Key** | Creates a key object from explicitly supplied attributes (`C_CreateObject`-style creation). |
| **Destroy Object** | Deletes the selected token object (`C_DestroyObject`). |
| **Edit Object** | Edits attributes of a selected object. Only attributes permitted by the token can be changed. |
| **Edit Attribute List** | Edits an object's attribute list in a batch-oriented editor. |
| **Copy Object** | Creates a copy of a selected object, optionally with changed attributes (`C_CopyObject`). |
| **Find Objects** | Searches the selected session for objects matching the specified attributes. |

## Cryptography

Run cryptographic operations through the loaded module and selected session or key.

| Command | Description |
|---|---|
| **Random** | Requests random bytes from the token's random-number generator (`C_GenerateRandom`). |
| **Digest** | Computes a message digest using a mechanism supported by the module. |
| **Signature** | Signs data with a selected private key and signature mechanism. |
| **Verify** | Verifies a signature against data using a selected public key and mechanism. |
| **Encrypt** | Encrypts data using a selected key and encryption mechanism. |
| **Decrypt** | Decrypts data using a selected key and decryption mechanism. |
| **HSM Manage** | Opens the HSM management interface for supported device-management operations. |

## Import

| Command | Description |
|---|---|
| **Import certificate** | Imports a certificate and creates a certificate object on the token. |
| **Import PFX** | Imports a PKCS #12/PFX bundle, which may contain a certificate chain and private key, subject to token support and bundle contents. |
| **Import Private Key** | Imports a private key from a supported key file and creates a key object on the token. |

## Tools

| Command | Description |
|---|---|
| **Initialize Token** | Initializes a token (`C_InitToken`), setting its label and security-officer PIN. Initialization may erase existing token contents. |
| **Operation State** | Gets or sets the saved state of an ongoing cryptographic operation when supported by the module. |
| **Set PIN** | Changes the user or security-officer PIN for the selected token (`C_SetPIN`). |
| **Init PIN** | Initializes the user PIN, typically after the security officer has logged in (`C_InitPIN`). |
| **Wrap Key** | Exports a key in wrapped (encrypted) form using a wrapping key and supported mechanism. |
| **Unwrap Key** | Imports a wrapped key and creates a key object using an unwrapping key and template. |
| **Derive Key** | Derives a new key from a base key and mechanism supported by the token. |
| **Type Name** | Displays or selects PKCS #11 type-name information used by the application. |
| **Make CSR** | Creates a certificate signing request (CSR), using a selected key and certificate-request fields. |
| **CAVP** | Opens the Cryptographic Algorithm Validation Program (CAVP) utility for supported validation vectors or operations. |

## Help

| Command | Description |
|---|---|
| **Clear Log** | Clears the messages shown in the log tab. |
| **Log** | Toggles log collection; the status tip describes the action as halting the log. |
| **Settings** | Opens CryptokiMan application settings. |
| **License Information** | Shows license details and status. |
| **Bug or Issue Report** | Opens the project's bug or issue reporting destination. |
| **Q and A** | Opens the project's question-and-answer or discussion destination. |
| **About CryptokiMan** | Shows application and version information. |

## Object context menu

Right-clicking an object row in the object table shows commands appropriate to that object's type. The exact set differs for certificates, public keys, private keys, secret keys, and other objects.

| Command | Description |
|---|---|
| **View Object** | Displays the selected object's attributes and details. |
| **Edit Attribute** | Edits an attribute of the selected object. |
| **Edit AttributeList** | Opens the attribute-list editor for the selected object. |
| **Delete Object** | Destroys the selected object on the token. |
| **View Certificate** | Displays certificate information. |
| **Copy Object** | Copies the selected object. |
| **Export Certficate** | Exports the selected certificate. |
| **Verify** | Verifies a signature using the selected public key. |
| **Encrypt** | Encrypts data using the selected public key. |
| **Export PublicKey** | Exports the selected public key. |
| **View PublicKey** | Displays public-key information. |
| **Sign** | Signs data using the selected private key. |
| **Decrypt** | Decrypts data using the selected private key. |
| **Export PrivateKey** | Exports the selected private key when permitted. |
| **View PrivateKey** | Displays private-key information and available attributes. |
| **Make CSR** | Creates a CSR using the selected private key. |

The object table may also offer **Verify**, **Encrypt**, **Sign**, or **Decrypt** for secret-key objects when the relevant operation is supported.
