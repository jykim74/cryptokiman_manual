# Unwrap Key Dialog

![Unwrap key dialog](../images/unwrap_key_dlg.png)

*Wrapped key input, unwrapping settings, and new-key attributes.*

## Purpose

Imports a wrapped key by selecting an unwrapping key and mechanism, providing the wrapped value, and defining the new key template.

## Fields and controls

| Control | Description |
|---|---|
| **Unwrap Key** | Input or information related to **Unwrap Key** for the current dialog operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **Input Clear** | Input or information related to **Input Clear** for the current dialog operation. |
| **Read File** | Input or information related to **Read File** for the current dialog operation. |
| **Wrapped Key Value** | Input or information related to **Wrapped Key Value** for the current dialog operation. |
| **Unwrap Key properties ( Decryption Key )** | Input or information related to **Unwrap Key properties ( Decryption Key )** for the current dialog operation. |
| **Label** | Human-readable label assigned to an object or key. |
| **Object** | Selected token object used as input or target. |
| **Type** | Input or information related to **Type** for the current dialog operation. |
| **Mechanism** | Cryptographic mechanism for the operation. |
| **Param** | Mechanism-specific parameters for the Cryptoki operation. |
| **Class** | PKCS #11 object class for a template or search. |
| **ID** | Object identifier used to associate or locate objects. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **Use Random** | Requests random key material rather than manually supplied material, where supported. |
| **Sensitive** | Marks private or secret key material as sensitive. |
| **Modifiable** | Allows object attributes to be modified. |
| **Unwrap** | Permits unwrapping keys. |
| **Derive** | Permits deriving other keys. |
| **Extractable** | Allows key material to be extracted when permitted by token policy. |
| **SignRecover** | Sets the corresponding **SignRecover** attribute or option for the operation. |
| **Sign** | Permits signing with this key. |
| **Verify** | Permits signature verification with this key. |
| **Wrap** | Permits wrapping other keys. |
| **Token** | When checked, stores the object as a token object; otherwise it is session-scoped. |
| **Decrypt** | Permits decryption with this key. |
| **Trusted** | Marks a public key as trusted where supported. |
| **VerifyRecover** | Sets the corresponding **VerifyRecover** attribute or option for the operation. |
| **Encrypt** | Permits encryption with this key. |
| **Private** | Marks an object private, subject to token login and policy. |
| **Destroyable** | Allows the object to be destroyed. |
| **EndDate** | Sets the corresponding **EndDate** attribute or option for the operation. |
| **Copyable** | Allows the object to be copied. |
| **StartDate** | Sets the corresponding **StartDate** attribute or option for the operation. |

## Typical use

Select an unwrapping key, choose a mechanism and parameters, load the wrapped value, configure the new-key template, and unwrap it.

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.
