# Create RSA Public Key Dialog

![Create RSA Public Key Dialog](../images/create_rsa_pub_key_dlg.png)

## Purpose

Creates an RSA public-key object from its modulus and public exponent, with configurable attributes.

## Fields and controls

| Control | Description |
|---|---|
| **Create RSA Public Key** | Input or information related to **Create RSA Public Key** for the current dialog operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **Subject** | Subject name associated with the key or certificate. |
| **Label** | Human-readable label assigned to an object or key. |
| **ID** | Object identifier used to associate or locate objects. |
| **Key Value** | Encoded key material. |
| **Key Length** | Requested or displayed key size, generally in bits. |
| **E** | Input or information related to **E** for the current dialog operation. |
| **Gen Key** | Input or information related to **Gen Key** for the current dialog operation. |
| **Find Key** | Input or information related to **Find Key** for the current dialog operation. |
| **Modules** | RSA modulus value. |
| **Exponent** | Input or information related to **Exponent** for the current dialog operation. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **Use SKI** | Sets the corresponding **Use SKI** attribute or option for the operation. |
| **Private** | Marks an object private, subject to token login and policy. |
| **VerifyRecover** | Sets the corresponding **VerifyRecover** attribute or option for the operation. |
| **Token** | When checked, stores the object as a token object; otherwise it is session-scoped. |
| **Encrypt** | Permits encryption with this key. |
| **Modifiable** | Allows object attributes to be modified. |
| **Trusted** | Marks a public key as trusted where supported. |
| **Derive** | Permits deriving other keys. |
| **Verify** | Permits signature verification with this key. |
| **Wrap** | Permits wrapping other keys. |
| **Destroyable** | Allows the object to be destroyed. |
| **EndDate** | Sets the corresponding **EndDate** attribute or option for the operation. |
| **Copyable** | Allows the object to be copied. |
| **StartDate** | Sets the corresponding **StartDate** attribute or option for the operation. |

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.

## Source files

- `create_rsa_pub_key_dlg.ui` defines the dialog layout and visible controls.
- `create_rsa_pub_key_dlg.cpp` implements dialog behavior and Cryptoki operations.
- `create_rsa_pub_key_dlg.h` declares the dialog class and interface.
