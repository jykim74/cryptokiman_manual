# Generate Key Pair Dialog

This guide describes the dialog implemented by `gen_key_pair_dlg.cpp`, `gen_key_pair_dlg.h`, and `gen_key_pair_dlg.ui`.

![Generate Key Pair Dialog](../images/gen_keypair_dlg.png)

## Purpose

Generates a public/private key pair on the selected token. Configure the mechanism and both key templates.

## Fields and controls

| Control | Description |
|---|---|
| **Generate Key Pair** | Input or information related to **Generate Key Pair** for the current dialog operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **Key size** | Requested key size for the generated key or pair. |
| **Mechanism** | Cryptographic mechanism for the operation. |
| **Gen Param** | Input or information related to **Gen Param** for the current dialog operation. |
| **Subprime(Q)** | Input or information related to **Subprime(Q)** for the current dialog operation. |
| **Prime(P)** | Input or information related to **Prime(P)** for the current dialog operation. |
| **Generator(G)** | Input or information related to **Generator(G)** for the current dialog operation. |
| **g** | Input or information related to **g** for the current dialog operation. |
| **Export** | Input or information related to **Export** for the current dialog operation. |
| **Gen DH Param** | Input or information related to **Gen DH Param** for the current dialog operation. |
| **p** | Input or information related to **p** for the current dialog operation. |
| **Import** | Input or information related to **Import** for the current dialog operation. |
| **Subject** | Subject name associated with the key or certificate. |
| **Label** | Human-readable label assigned to an object or key. |
| **ID** | Object identifier used to associate or locate objects. |
| **PubKeyInfo** | Input or information related to **PubKeyInfo** for the current dialog operation. |
| **Same Label** | Input or information related to **Same Label** for the current dialog operation. |
| **Exponent** | Input or information related to **Exponent** for the current dialog operation. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **Use SKI** | Sets the corresponding **Use SKI** attribute or option for the operation. |
| **Use SPKI** | Sets the corresponding **Use SPKI** attribute or option for the operation. |
| **Modifiable** | Allows object attributes to be modified. |
| **Unwrap** | Permits unwrapping keys. |
| **Sign** | Permits signing with this key. |
| **Token** | When checked, stores the object as a token object; otherwise it is session-scoped. |
| **Sensitive** | Marks private or secret key material as sensitive. |
| **Decrypt** | Permits decryption with this key. |
| **Extractable** | Allows key material to be extracted when permitted by token policy. |
| **SignRecover** | Sets the corresponding **SignRecover** attribute or option for the operation. |
| **Derive** | Permits deriving other keys. |
| **Private** | Marks an object private, subject to token login and policy. |
| **Copyable** | Allows the object to be copied. |
| **Destroyable** | Allows the object to be destroyed. |
| **EndDate** | Sets the corresponding **EndDate** attribute or option for the operation. |
| **StartDate** | Sets the corresponding **StartDate** attribute or option for the operation. |
| **Verify** | Permits signature verification with this key. |
| **Trusted** | Marks a public key as trusted where supported. |
| **Wrap** | Permits wrapping other keys. |
| **Encrypt** | Permits encryption with this key. |
| **VerifyRecover** | Sets the corresponding **VerifyRecover** attribute or option for the operation. |

## Typical use

Choose a mechanism and key size, configure public and private key templates, and generate the pair.

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.

## Source files

- `gen_key_pair_dlg.ui` defines the dialog layout and visible controls.
- `gen_key_pair_dlg.cpp` implements dialog behavior and Cryptoki operations.
- `gen_key_pair_dlg.h` declares the dialog class and interface.
