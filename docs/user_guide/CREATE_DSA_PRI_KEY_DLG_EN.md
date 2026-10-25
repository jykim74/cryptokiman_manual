# Create DSA Private Key Dialog

![Create DSA private key dialog](../images/create_dsa_pri_key_dlg.png)

*DSA private-key fields and usage attributes.*

## Purpose

Creates a DSA private-key object with key material, identifying information, and private-key usage attributes.

## Fields and controls

| Control | Description |
|---|---|
| **Create DSA Private Key** | Input or information related to **Create DSA Private Key** for the current dialog operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **Label** | Human-readable label assigned to an object or key. |
| **ID** | Object identifier used to associate or locate objects. |
| **Subject** | Subject name associated with the key or certificate. |
| **PubKeyInfo** | Input or information related to **PubKeyInfo** for the current dialog operation. |
| **Key Length** | Requested or displayed key size, generally in bits. |
| **Key Value** | Encoded key material. |
| **Gen Key** | Input or information related to **Gen Key** for the current dialog operation. |
| **Find Key** | Input or information related to **Find Key** for the current dialog operation. |
| **Key value** | Input or information related to **Key value** for the current dialog operation. |
| **Subprime(Q)** | Input or information related to **Subprime(Q)** for the current dialog operation. |
| **Base(G)** | Input or information related to **Base(G)** for the current dialog operation. |
| **Prime(P)** | Input or information related to **Prime(P)** for the current dialog operation. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **Use SKI** | Sets the corresponding **Use SKI** attribute or option for the operation. |
| **Use SPKI** | Sets the corresponding **Use SPKI** attribute or option for the operation. |
| **Modifiable** | Allows object attributes to be modified. |
| **SignRecover** | Sets the corresponding **SignRecover** attribute or option for the operation. |
| **Derive** | Permits deriving other keys. |
| **Unwrap** | Permits unwrapping keys. |
| **Private** | Marks an object private, subject to token login and policy. |
| **Sensitive** | Marks private or secret key material as sensitive. |
| **Extractable** | Allows key material to be extracted when permitted by token policy. |
| **Decrypt** | Permits decryption with this key. |
| **Sign** | Permits signing with this key. |
| **Token** | When checked, stores the object as a token object; otherwise it is session-scoped. |
| **Destroyable** | Allows the object to be destroyed. |
| **Copyable** | Allows the object to be copied. |
| **StartDate** | Sets the corresponding **StartDate** attribute or option for the operation. |
| **EndDate** | Sets the corresponding **EndDate** attribute or option for the operation. |

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.
