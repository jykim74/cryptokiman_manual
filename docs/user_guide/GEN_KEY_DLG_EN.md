# Generate Key Dialog

![Generate Key Dialog](../images/gen_key_dlg.png)

## Purpose

Generates a key on the selected token using a mechanism, key size, parameters, and object attributes.

## Fields and controls

| Control | Description |
|---|---|
| **Generate Key** | Input or information related to **Generate Key** for the current dialog operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **Key size** | Requested key size for the generated key or pair. |
| **Mechanism** | Cryptographic mechanism for the operation. |
| **Parameter** | Mechanism-specific parameters for the Cryptoki operation. |
| **Label** | Human-readable label assigned to an object or key. |
| **ID** | Object identifier used to associate or locate objects. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **Use Random** | Requests random key material rather than manually supplied material, where supported. |
| **Modifiable** | Allows object attributes to be modified. |
| **Derive** | Permits deriving other keys. |
| **Extractable** | Allows key material to be extracted when permitted by token policy. |
| **Sensitive** | Marks private or secret key material as sensitive. |
| **Unwrap** | Permits unwrapping keys. |
| **Private** | Marks an object private, subject to token login and policy. |
| **Wrap** | Permits wrapping other keys. |
| **Encrypt** | Permits encryption with this key. |
| **Verify** | Permits signature verification with this key. |
| **Decrypt** | Permits decryption with this key. |
| **Trusted** | Marks a public key as trusted where supported. |
| **Token** | When checked, stores the object as a token object; otherwise it is session-scoped. |
| **Sign** | Permits signing with this key. |
| **Destroyable** | Allows the object to be destroyed. |
| **EndDate** | Sets the corresponding **EndDate** attribute or option for the operation. |
| **Copyable** | Allows the object to be copied. |
| **StartDate** | Sets the corresponding **StartDate** attribute or option for the operation. |

## Typical use

Choose a mechanism and key size, set key-template attributes, and start key generation.

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.

## Source files

- `gen_key_dlg.ui` defines the dialog layout and visible controls.
- `gen_key_dlg.cpp` implements dialog behavior and Cryptoki operations.
- `gen_key_dlg.h` declares the dialog class and interface.
