# Create Key Object Dialog


![Create key dialog](../images/create_key_dlg.png)

*Key information and attributes for a new key object.*

## Purpose

Creates a key object from selected key information and object attributes.

## Fields and controls

| Control | Description |
|---|---|
| **Create Key Object** | Input or information related to **Create Key Object** for the current dialog operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **Key Information** | Input or information related to **Key Information** for the current dialog operation. |
| **Key** | Key value or selected key information. |
| **Label** | Human-readable label assigned to an object or key. |
| **ID** | Object identifier used to associate or locate objects. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **Use Random** | Requests random key material rather than manually supplied material, where supported. |
| **Encrypt** | Permits encryption with this key. |
| **Trusted** | Marks a public key as trusted where supported. |
| **Extractable** | Allows key material to be extracted when permitted by token policy. |
| **Sign** | Permits signing with this key. |
| **Derive** | Permits deriving other keys. |
| **Sensitive** | Marks private or secret key material as sensitive. |
| **Verify** | Permits signature verification with this key. |
| **Modifiable** | Allows object attributes to be modified. |
| **Wrap** | Permits wrapping other keys. |
| **Token** | When checked, stores the object as a token object; otherwise it is session-scoped. |
| **Private** | Marks an object private, subject to token login and policy. |
| **Unwrap** | Permits unwrapping keys. |
| **Decrypt** | Permits decryption with this key. |
| **Destroyable** | Allows the object to be destroyed. |
| **EndDate** | Sets the corresponding **EndDate** attribute or option for the operation. |
| **Copyable** | Allows the object to be copied. |
| **StartDate** | Sets the corresponding **StartDate** attribute or option for the operation. |

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.
