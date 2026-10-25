# Find Objects Dialog

![Find objects dialog](../images/find_object_dlg.png)

*Object filters for searching the selected session.*

## Purpose

Searches the selected session for objects matching the specified object class, identifying fields, and attribute values.

## Fields and controls

| Control | Description |
|---|---|
| **Find Objects** | Input or information related to **Find Objects** for the current dialog operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **Max Count** | Maximum number of matching objects to return. |
| **Class** | PKCS #11 object class for a template or search. |
| **Key Type** | PKCS #11 key type or operation key category. |
| **Subject** | Subject name associated with the key or certificate. |
| **Label** | Human-readable label assigned to an object or key. |
| **ID** | Object identifier used to associate or locate objects. |
| **PubKeyInfo** | Input or information related to **PubKeyInfo** for the current dialog operation. |
| **Application** | Application attribute for a PKCS #11 data object. |
| **Object ID** | PKCS #11 object identifier attribute. |
| **Find Objets** | Input or information related to **Find Objets** for the current dialog operation. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **Wrap** | Permits wrapping other keys. |
| **Encrypt** | Permits encryption with this key. |
| **EndDate** | Sets the corresponding **EndDate** attribute or option for the operation. |
| **Modifiable** | Allows object attributes to be modified. |
| **Unwrap** | Permits unwrapping keys. |
| **StartDate** | Sets the corresponding **StartDate** attribute or option for the operation. |
| **Sensitive** | Marks private or secret key material as sensitive. |
| **Extractable** | Allows key material to be extracted when permitted by token policy. |
| **Destroyable** | Allows the object to be destroyed. |
| **Verify** | Permits signature verification with this key. |
| **Private** | Marks an object private, subject to token login and policy. |
| **Copyable** | Allows the object to be copied. |
| **Sign** | Permits signing with this key. |
| **Trusted** | Marks a public key as trusted where supported. |
| **Decrypt** | Permits decryption with this key. |
| **Derive** | Permits deriving other keys. |
| **Token** | When checked, stores the object as a token object; otherwise it is session-scoped. |

## Typical use

Set search criteria and a maximum result count, then choose Find Objects to search the current session.

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.
