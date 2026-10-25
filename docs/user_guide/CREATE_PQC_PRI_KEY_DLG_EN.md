# Create PQC Private Key Dialog

![Create PQC Private Key Dialog](../images/create_pqc_pri_key_dlg.png)

## Purpose

Creates a post-quantum cryptography private-key object for a supported algorithm and parameter set.

## Fields and controls

| Control | Description |
|---|---|
| **Create PQC Private Key** | Input or information related to **Create PQC Private Key** for the current dialog operation. |
| **Algorithm** | Algorithm family for the test or key operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **ID** | Object identifier used to associate or locate objects. |
| **PubKeyInfo** | Input or information related to **PubKeyInfo** for the current dialog operation. |
| **Subject** | Subject name associated with the key or certificate. |
| **Label** | Human-readable label assigned to an object or key. |
| **Gen Key** | Input or information related to **Gen Key** for the current dialog operation. |
| **Find Key** | Input or information related to **Find Key** for the current dialog operation. |
| **Parameter Set** | Algorithm parameter set for the post-quantum key. |
| **Key Value** | Encoded key material. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **Use SKI** | Sets the corresponding **Use SKI** attribute or option for the operation. |
| **Use SPKI** | Sets the corresponding **Use SPKI** attribute or option for the operation. |
| **Derive** | Permits deriving other keys. |
| **Decrypt** | Permits decryption with this key. |
| **Destroyable** | Allows the object to be destroyed. |
| **Token** | When checked, stores the object as a token object; otherwise it is session-scoped. |
| **Modifiable** | Allows object attributes to be modified. |
| **SignRecover** | Sets the corresponding **SignRecover** attribute or option for the operation. |
| **StartDate** | Sets the corresponding **StartDate** attribute or option for the operation. |
| **EndDate** | Sets the corresponding **EndDate** attribute or option for the operation. |
| **Sign** | Permits signing with this key. |
| **Sensitive** | Marks private or secret key material as sensitive. |
| **Extractable** | Allows key material to be extracted when permitted by token policy. |
| **Private** | Marks an object private, subject to token login and policy. |
| **Unwrap** | Permits unwrapping keys. |
| **Copyable** | Allows the object to be copied. |

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.

## Source files

- `create_pqc_pri_key_dlg.ui` defines the dialog layout and visible controls.
- `create_pqc_pri_key_dlg.cpp` implements dialog behavior and Cryptoki operations.
- `create_pqc_pri_key_dlg.h` declares the dialog class and interface.
