# Edit Attribute List Dialog

![Edit attribute list dialog](../images/edit_attribute_list_dlg.png)

*A selection of object attributes to read or update.*

## Purpose

Reads or updates a selected set of common object attributes in one operation.

## Fields and controls

| Control | Description |
|---|---|
| **Edit Attribute List** | Input or information related to **Edit Attribute List** for the current dialog operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **GetAttribute** | Input or information related to **GetAttribute** for the current dialog operation. |
| **SetAttribute** | Input or information related to **SetAttribute** for the current dialog operation. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **Class** | PKCS #11 object class for a template or search. |
| **Key Type** | PKCS #11 key type or operation key category. |
| **Label** | Human-readable label assigned to an object or key. |
| **Application** | Application attribute for a PKCS #11 data object. |
| **Object ID** | PKCS #11 object identifier attribute. |
| **ID** | Object identifier used to associate or locate objects. |
| **Modifiable** | Allows object attributes to be modified. |
| **Trusted** | Marks a public key as trusted where supported. |
| **StartDate** | Sets the corresponding **StartDate** attribute or option for the operation. |
| **Unwrap** | Permits unwrapping keys. |
| **Token** | When checked, stores the object as a token object; otherwise it is session-scoped. |
| **Private** | Marks an object private, subject to token login and policy. |
| **Sensitive** | Marks private or secret key material as sensitive. |
| **Wrap** | Permits wrapping other keys. |
| **Encrypt** | Permits encryption with this key. |
| **Sign** | Permits signing with this key. |
| **Extractable** | Allows key material to be extracted when permitted by token policy. |
| **Copyable** | Allows the object to be copied. |
| **EndDate** | Sets the corresponding **EndDate** attribute or option for the operation. |
| **Decrypt** | Permits decryption with this key. |
| **Verify** | Permits signature verification with this key. |
| **Derive** | Permits deriving other keys. |
| **Destroyable** | Allows the object to be destroyed. |

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.
