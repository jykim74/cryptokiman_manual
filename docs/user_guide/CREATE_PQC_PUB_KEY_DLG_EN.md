# Create PQC Public Key Dialog

This guide describes the dialog implemented by `create_pqc_pub_key_dlg.cpp`, `create_pqc_pub_key_dlg.h`, and `create_pqc_pub_key_dlg.ui`.

![Create PQC Public Key Dialog](../images/create_pqc_pub_key_dlg.png)

## Purpose

Creates a post-quantum cryptography public-key object for a supported algorithm and parameter set.

## Fields and controls

| Control | Description |
|---|---|
| **Create PQC Public Key** | Input or information related to **Create PQC Public Key** for the current dialog operation. |
| **Algorithm** | Algorithm family for the test or key operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **Label** | Human-readable label assigned to an object or key. |
| **ID** | Object identifier used to associate or locate objects. |
| **Subject** | Subject name associated with the key or certificate. |
| **Parameter Set** | Algorithm parameter set for the post-quantum key. |
| **Gen Key** | Input or information related to **Gen Key** for the current dialog operation. |
| **Find Key** | Input or information related to **Find Key** for the current dialog operation. |
| **Key Value** | Encoded key material. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **Use SKI** | Sets the corresponding **Use SKI** attribute or option for the operation. |
| **Verify** | Permits signature verification with this key. |
| **EndDate** | Sets the corresponding **EndDate** attribute or option for the operation. |
| **Copyable** | Allows the object to be copied. |
| **Encrypt** | Permits encryption with this key. |
| **Wrap** | Permits wrapping other keys. |
| **Token** | When checked, stores the object as a token object; otherwise it is session-scoped. |
| **Private** | Marks an object private, subject to token login and policy. |
| **Derive** | Permits deriving other keys. |
| **VerifyRecover** | Sets the corresponding **VerifyRecover** attribute or option for the operation. |
| **Trusted** | Marks a public key as trusted where supported. |
| **Modifiable** | Allows object attributes to be modified. |
| **Destroyable** | Allows the object to be destroyed. |
| **StartDate** | Sets the corresponding **StartDate** attribute or option for the operation. |

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.

## Source files

- `create_pqc_pub_key_dlg.ui` defines the dialog layout and visible controls.
- `create_pqc_pub_key_dlg.cpp` implements dialog behavior and Cryptoki operations.
- `create_pqc_pub_key_dlg.h` declares the dialog class and interface.
