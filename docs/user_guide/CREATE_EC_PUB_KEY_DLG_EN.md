# Create ECDSA Public Key Dialog

This guide describes the dialog implemented by `create_ec_pub_key_dlg.cpp`, `create_ec_pub_key_dlg.h`, and `create_ec_pub_key_dlg.ui`.

![Create ECDSA Public Key Dialog](../images/create_ec_pub_key_dlg.png)

## Purpose

Creates an elliptic-curve public-key object with curve and point information and public-key usage attributes.

## Fields and controls

| Control | Description |
|---|---|
| **Create ECDSA Public Key** | Input or information related to **Create ECDSA Public Key** for the current dialog operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **Label** | Human-readable label assigned to an object or key. |
| **ID** | Object identifier used to associate or locate objects. |
| **Subject** | Subject name associated with the key or certificate. |
| **Gen Key** | Input or information related to **Gen Key** for the current dialog operation. |
| **Key Value** | Encoded key material. |
| **Named Curve** | Elliptic curve selected for the EC key. |
| **Find Key** | Input or information related to **Find Key** for the current dialog operation. |
| **EC Points** | Encoded elliptic-curve public point. |
| **EC Params** | Encoded elliptic-curve domain parameters. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **Use SKI** | Sets the corresponding **Use SKI** attribute or option for the operation. |
| **Modifiable** | Allows object attributes to be modified. |
| **VerifyRecover** | Sets the corresponding **VerifyRecover** attribute or option for the operation. |
| **Token** | When checked, stores the object as a token object; otherwise it is session-scoped. |
| **Verify** | Permits signature verification with this key. |
| **Encrypt** | Permits encryption with this key. |
| **Private** | Marks an object private, subject to token login and policy. |
| **Trusted** | Marks a public key as trusted where supported. |
| **Derive** | Permits deriving other keys. |
| **Wrap** | Permits wrapping other keys. |
| **Destroyable** | Allows the object to be destroyed. |
| **EndDate** | Sets the corresponding **EndDate** attribute or option for the operation. |
| **Copyable** | Allows the object to be copied. |
| **StartDate** | Sets the corresponding **StartDate** attribute or option for the operation. |

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.

## Source files

- `create_ec_pub_key_dlg.ui` defines the dialog layout and visible controls.
- `create_ec_pub_key_dlg.cpp` implements dialog behavior and Cryptoki operations.
- `create_ec_pub_key_dlg.h` declares the dialog class and interface.
