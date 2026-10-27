# CryptokiMan Menu Guide

This guide summarizes CryptokiMan's menus and the actions they provide for tokens, sessions, objects, and cryptographic operations.

## File

| Command | Description |
|---|---|
| **New** | Opens another CryptokiMan window. |
| [**Open...**](MAINWINDOW_EN.md) | Selects and loads a Cryptoki library. Only one library can be loaded at a time. |
| [**Unload**](MAINWINDOW_EN.md) | Unloads the currently loaded Cryptoki library. |
| [**Show log tab**](MAINWINDOW_EN.md) | Shows the Information and Log dock at the bottom of the window. |
| **Recent Files** | Opens a previously loaded library. The menu keeps up to ten recent entries. |
| **Quit** | Exits CryptokiMan. |

## View

The [**View**](MAINWINDOW_EN.md) menu is available when the application has a valid license. Its submenus contain checkable options for showing or hiding individual buttons on the File, Module, Object, Cryptogram, Import, Tools, and Help toolbars. The Cryptogram toolbar contains the **Cryptography** menu commands. Changing a toolbar option does not remove the command from its main menu.

## Module

| Command | Description |
|---|---|
| **Initialize** | Initializes the PKCS #11 library (`C_Initialize`). |
| **Finalize** | Finalizes the PKCS #11 library (`C_Finalize`). |
| [**Open Session**](OPEN_SESSION_DLG_EN.md) | Opens a session on the selected token (`C_OpenSession`). |
| [**Close Session**](CLOSE_SESSION_DLG_EN.md) | Closes the selected session (`C_CloseSession`). |
| [**Close All Sessions**](CLOSE_SESSION_DLG_EN.md) | Closes all sessions for the selected token (`C_CloseAllSessions`). |
| [**Login**](LOGIN_DLG_EN.md) | Logs in to the selected session, for example as a user or security officer (`C_Login`). |
| [**Logout**](LOGOUT_DLG_EN.md) | Logs out of the selected session (`C_Logout`). |

## Objects

| Command | Description |
|---|---|
| [**Generate Key Pair**](GEN_KEYPAIR_DLG_EN.md) | Generates a public/private key pair on the token (`C_GenerateKeyPair`). |
| [**Generate Key**](GEN_KEY_DLG_EN.md) | Generates a secret key on the token (`C_GenerateKey`). |
| [**Create Data**](CREATE_DATA_DLG_EN.md) | Creates a data object using the supplied attributes (`C_CreateObject`). |
| [**Create RSA Public Key**](CREATE_RSA_PUB_KEY_DLG_EN.md) | Creates an RSA public-key object from supplied attributes. |
| [**Create RSA Private Key**](CREATE_RSA_PRI_KEY_DLG_EN.md) | Creates an RSA private-key object from supplied attributes. |
| [**Create ECDSA Public Key**](CREATE_EC_PUB_KEY_DLG_EN.md) | Creates an elliptic-curve public-key object, commonly used for ECDSA. |
| [**Create ECDSA Private Key**](CREATE_EC_PRI_KEY_DLG_EN.md) | Creates an elliptic-curve private-key object, commonly used for ECDSA. |
| **Create EDDSA Public Key** | Creates an Edwards-curve digital-signature public-key object. |
| **Create EDDSA Private Key** | Creates an Edwards-curve digital-signature private-key object. |
| [**Create DSA Public Key**](CREATE_DSA_PUB_KEY_DLG_EN.md) | Creates a DSA public-key object from supplied attributes. |
| [**Create DSA Private Key**](CREATE_DSA_PRI_KEY_DLG_EN.md) | Creates a DSA private-key object from supplied attributes. |
| [**Create PQC Public Key**](CREATE_PQC_PUB_KEY_DLG_EN.md) | Creates a post-quantum cryptography public-key object supported by the library. |
| [**Create PQC Private Key**](CREATE_PQC_PRI_KEY_DLG_EN.md) | Creates a post-quantum cryptography private-key object supported by the library. |
| [**Create Key**](CREATE_KEY_DLG_EN.md) | Creates a key object from a supplied template. |
| [**Destroy Object**](DEL_OBJECT_DLG_EN.md) | Destroys the selected token object (`C_DestroyObject`). |
| [**Edit Object**](EDIT_ATTRIBUTE_DLG_EN.md) | Edits attributes of the selected object. Whether an attribute can be changed depends on the token. |
| [**Edit Attribute List**](EDIT_ATTRIBUTE_LIST_DLG_EN.md) | Edits a list of attributes for the selected object. |
| [**Copy Object**](COPY_OBJECT_DLG_EN.md) | Copies the selected object, optionally with changed attributes (`C_CopyObject`). |
| [**Find Objects**](FIND_OBJECT_DLG_EN.md) | Searches the selected session for objects matching supplied attributes. |

## Cryptography

| Command | Description |
|---|---|
| [**Random**](RAND_DLG_EN.md) | Generates random bytes using the token (`C_GenerateRandom`). |
| [**Digest**](DIGEST_DLG_EN.md) | Computes a message digest using a supported mechanism. |
| [**Signature**](SIGN_DLG_EN.md) | Signs data using a selected private key and signature mechanism. |
| [**Verify**](VERIFY_DLG_EN.md) | Verifies a signature using data, a signature, and a suitable public key. |
| [**Encrypt**](ENCRYPT_DLG_EN.md) | Encrypts data using a selected key and supported mechanism. |
| [**Decrypt**](DECRYPT_DLG_EN.md) | Decrypts data using a selected key and supported mechanism. |
| [**HSM Manage**](HSM_MAN_DLG_EN.md) | Opens the HSM management window. Available management operations depend on the configured HSM. |

## Import

| Command | Description |
|---|---|
| [**Import certificate**](IMPORT_CERT_DLG_EN.md) | Imports a certificate and creates a certificate object on the token. |
| [**Import PFX**](IMPORT_PFX_DLG_EN.md) | Imports a PKCS #12/PFX file. The file may contain certificates and a private key. |
| [**Import Private Key**](IMPORT_PRI_KEY_DLG_EN.md) | Imports a supported private-key file and creates a key object on the token. |

## Tools

| Command | Description |
|---|---|
| [**Initialize Token**](INIT_TOKEN_DLG_EN.md) | Initializes the selected token (`C_InitToken`), including its label and security-officer PIN. Token initialization may erase existing token data. |
| [**Operation State**](OPER_STATE_DLG_EN.md) | Reads or restores the state of an operation when supported by the token. |
| [**Set PIN**](SET_PIN_DLG_EN.md) | Changes a token PIN (`C_SetPIN`). |
| [**Init PIN**](INIT_PIN_DLG_EN.md) | Initializes the user PIN (`C_InitPIN`), generally after security-officer authentication. |
| [**Wrap Key**](WRAP_KEY_DLG_EN.md) | Wraps (exports in encrypted form) a key using a wrapping key and supported mechanism. |
| [**Unwrap Key**](UNWRAP_KEY_DLG_EN.md) | Unwraps a key and creates a corresponding key object on the token. |
| [**Derive Key**](DERIVE_KEY_DLG_EN.md) | Derives a new key from a base key using a supported mechanism. |
| [**Type Name**](TYPE_NAME_DLG_EN.md) | Opens the type-name utility for PKCS #11 type information. |
| [**Make CSR**](MAKE_CSR_DLG_EN.md) | Creates a certificate signing request (CSR) using a key and request details. |
| [**CAVP**](CAVP_DLG_EN.md) | Opens the Cryptographic Algorithm Validation Program utility. |

## Help

| Command | Description |
|---|---|
| **Clear Log** | Clears the messages in the Log tab. This command is created when a valid license is present. |
| **Log** | Toggles logging. The command's status tip says “Halt log”; it is created when a valid license is present. |
| [**Settings**](SETTINGS_DLG_EN.md) | Opens CryptokiMan settings. |
| [**License Information**](LCN_INFO_DLG_EN.md) | Displays license information. |
| **Bug or Issue Report** | Opens the project's bug or issue reporting page. |
| **Q and A** | Opens the project's Q&A or discussion page. |
| **About CryptokiMan** | Displays information about the application. |

## Object table context menu

Right-click an object row to show commands for that object type. The menu is not shown for the root, slot, token, mechanism, or session tree items.

| Command | Description |
|---|---|
| **View Object** | Displays details of the selected object. |
| [**Edit Attribute**](EDIT_ATTRIBUTE_DLG_EN.md) | Edits an attribute of the selected object. |
| [**Edit AttributeList**](EDIT_ATTRIBUTE_LIST_DLG_EN.md) | Opens the attribute-list editor. |
| [**Delete Object**](DEL_OBJECT_DLG_EN.md) | Destroys the selected object. |
| **View Certificate** | Displays certificate details. Shown for certificate objects. |
| **Export Certficate** | Exports a certificate object. Shown for certificate objects. |
| [**Verify**](VERIFY_DLG_EN.md) / [**Encrypt**](ENCRYPT_DLG_EN.md) | Uses a public key for signature verification or encryption. Shown for public-key objects. |
| **Export PublicKey / View PublicKey** | Exports or displays a public key. |
| [**Sign**](SIGN_DLG_EN.md) / [**Decrypt**](DECRYPT_DLG_EN.md) | Uses a private key to sign or decrypt. Shown for private-key objects. |
| **Export PrivateKey / View PrivateKey** | Exports or displays a private key, subject to token permissions. |
| [**Make CSR**](MAKE_CSR_DLG_EN.md) | Creates a CSR using a private-key object. |
| [**Sign**](SIGN_DLG_EN.md) / [**Verify**](VERIFY_DLG_EN.md) / [**Encrypt**](ENCRYPT_DLG_EN.md) / [**Decrypt**](DECRYPT_DLG_EN.md) | Offers supported cryptographic operations for a secret-key object. |
| [**Copy Object**](COPY_OBJECT_DLG_EN.md) | Copies the selected object. Available for certificate, public-key, private-key, secret-key, and data objects. |

Commands may be disabled when the license does not enable the operation. Actual success also depends on the PKCS #11 module, token, session state, key attributes, and mechanism support.
