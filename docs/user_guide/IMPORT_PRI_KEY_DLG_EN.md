# Import Private Key Dialog

This guide describes the dialog implemented by `import_pri_key_dlg.cpp`, `import_pri_key_dlg.h`, and `import_pri_key_dlg.ui`.

![Import Private Key Dialog](../images/import_pri_key_dlg.png)

## Purpose

Imports a supported private-key file. You can provide a password for encrypted input and configure the key attributes.

## Fields and controls

| Control | Description |
|---|---|
| **Import Private Key** | Input or information related to **Import Private Key** for the current dialog operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **Path** | Input file path. |
| **Password** | Password used to access or decrypt the selected input file. |
| **Private Key Attributes** | Input or information related to **Private Key Attributes** for the current dialog operation. |
| **Label** | Human-readable label assigned to an object or key. |
| **ID** | Object identifier used to associate or locate objects. |
| **Subject** | Subject name associated with the key or certificate. |
| **PubKeyInfo** | Input or information related to **PubKeyInfo** for the current dialog operation. |
| **Same Label** | Input or information related to **Same Label** for the current dialog operation. |
| **Public Key Attributes** | Input or information related to **Public Key Attributes** for the current dialog operation. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **Encrypted PrivateKey** | Sets the corresponding **Encrypted PrivateKey** attribute or option for the operation. |
| **Save public key from private key** | Sets the corresponding **Save public key from private key** attribute or option for the operation. |
| **Use SKI** | Sets the corresponding **Use SKI** attribute or option for the operation. |
| **Use SPKI** | Sets the corresponding **Use SPKI** attribute or option for the operation. |
| **Token** | When checked, stores the object as a token object; otherwise it is session-scoped. |
| **Modifiable** | Allows object attributes to be modified. |
| **Unwrap** | Permits unwrapping keys. |
| **Derive** | Permits deriving other keys. |
| **Extractable** | Allows key material to be extracted when permitted by token policy. |
| **SignRecover** | Sets the corresponding **SignRecover** attribute or option for the operation. |
| **Decrypt** | Permits decryption with this key. |
| **Private** | Marks an object private, subject to token login and policy. |
| **Sensitive** | Marks private or secret key material as sensitive. |
| **Sign** | Permits signing with this key. |
| **Copyable** | Allows the object to be copied. |
| **StartDate** | Sets the corresponding **StartDate** attribute or option for the operation. |
| **Destroyable** | Allows the object to be destroyed. |
| **EndDate** | Sets the corresponding **EndDate** attribute or option for the operation. |
| **Wrap** | Permits wrapping other keys. |
| **Verify** | Permits signature verification with this key. |
| **Encrypt** | Permits encryption with this key. |
| **VerifyRecover** | Sets the corresponding **VerifyRecover** attribute or option for the operation. |
| **Trusted** | Marks a public key as trusted where supported. |

## Typical use

Select the key file, enter its password if needed, choose whether to save its public key, configure attributes, and import.

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.

## Source files

- `import_pri_key_dlg.ui` defines the dialog layout and visible controls.
- `import_pri_key_dlg.cpp` implements dialog behavior and Cryptoki operations.
- `import_pri_key_dlg.h` declares the dialog class and interface.
