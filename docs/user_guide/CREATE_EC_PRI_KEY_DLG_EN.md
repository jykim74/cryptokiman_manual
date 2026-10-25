# Create ECDSA Private Key Dialog

![Create EC private key dialog](../images/create_ec_pri_key_dlg.png)

*EC private-key fields, curve parameters, and usage attributes.*

## Purpose

Creates an elliptic-curve private-key object, including curve parameters and private-key usage attributes.

## Fields and controls

| Control | Description |
|---|---|
| **Create ECDSA Private Key** | Input or information related to **Create ECDSA Private Key** for the current dialog operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **Subject** | Subject name associated with the key or certificate. |
| **ID** | Object identifier used to associate or locate objects. |
| **Label** | Human-readable label assigned to an object or key. |
| **PubKeyInfo** | Input or information related to **PubKeyInfo** for the current dialog operation. |
| **Gen Key** | Input or information related to **Gen Key** for the current dialog operation. |
| **Key Value** | Encoded key material. |
| **Named Curve** | Elliptic curve selected for the EC key. |
| **Find Key** | Input or information related to **Find Key** for the current dialog operation. |
| **EC Params** | Encoded elliptic-curve domain parameters. |
| **Key value** | Input or information related to **Key value** for the current dialog operation. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **Use SKI** | Sets the corresponding **Use SKI** attribute or option for the operation. |
| **Use SPKI** | Sets the corresponding **Use SPKI** attribute or option for the operation. |
| **Token** | When checked, stores the object as a token object; otherwise it is session-scoped. |
| **Unwrap** | Permits unwrapping keys. |
| **Sign** | Permits signing with this key. |
| **SignRecover** | Sets the corresponding **SignRecover** attribute or option for the operation. |
| **Modifiable** | Allows object attributes to be modified. |
| **Private** | Marks an object private, subject to token login and policy. |
| **Extractable** | Allows key material to be extracted when permitted by token policy. |
| **Derive** | Permits deriving other keys. |
| **Decrypt** | Permits decryption with this key. |
| **Sensitive** | Marks private or secret key material as sensitive. |
| **Copyable** | Allows the object to be copied. |
| **StartDate** | Sets the corresponding **StartDate** attribute or option for the operation. |
| **Destroyable** | Allows the object to be destroyed. |
| **EndDate** | Sets the corresponding **EndDate** attribute or option for the operation. |

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.
