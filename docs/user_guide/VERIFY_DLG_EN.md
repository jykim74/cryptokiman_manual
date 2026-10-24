# Verify Signature Dialog

This guide describes the dialog implemented by `verify_dlg.cpp`, `verify_dlg.h`, and `verify_dlg.ui`.

![Verify Signature Dialog](../images/verify_dlg.png)

## Purpose

Verifies a signature using a selected public key and mechanism. Input can be entered directly or read from a file.

## Fields and controls

| Control | Description |
|---|---|
| **Verify Signature** | Input or information related to **Verify Signature** for the current dialog operation. |
| **Slot Info** | Read-only information identifying the selected token slot. |
| **Mechanism** | Cryptographic mechanism for the operation. |
| **Key Type** | PKCS #11 key type or operation key category. |
| **Param** | Mechanism-specific parameters for the Cryptoki operation. |
| **MGF1** | Input or information related to **MGF1** for the current dialog operation. |
| **Len** | Input or information related to **Len** for the current dialog operation. |
| **hashAlg** | Input or information related to **hashAlg** for the current dialog operation. |
| **Label** | Human-readable label assigned to an object or key. |
| **Object** | Selected token object used as input or target. |
| **C** | Input or information related to **C** for the current dialog operation. |
| **Input** | Input data for the selected operation. |
| **Update** | Input or information related to **Update** for the current dialog operation. |
| **VerifyRecover** | Input or information related to **VerifyRecover** for the current dialog operation. |
| **VerifyRecoverInit** | Input or information related to **VerifyRecoverInit** for the current dialog operation. |
| **Final** | Input or information related to **Final** for the current dialog operation. |
| **Src File Path** | Optional input file path. |
| **File Information** | Input or information related to **File Information** for the current dialog operation. |
| **Total File Size** | Input or information related to **Total File Size** for the current dialog operation. |
| **Read File Size** | Input or information related to **Read File Size** for the current dialog operation. |
| **File Status** | Input or information related to **File Status** for the current dialog operation. |
| **Run Status** | Input or information related to **Run Status** for the current dialog operation. |
| **Init** | Input or information related to **Init** for the current dialog operation. |
| **Reset** | Input or information related to **Reset** for the current dialog operation. |
| **Signature** | Input or information related to **Signature** for the current dialog operation. |
| **Verify** | Permits signature verification with this key. |
| **Status** | Input or information related to **Status** for the current dialog operation. |

### Object and operation attributes

These checkboxes configure the object template or operation. Their effect depends on token capabilities and permissions.

| Option | Meaning |
|---|---|
| **RunThread** | Sets the corresponding **RunThread** attribute or option for the operation. |
| **Init Automatically** | Sets the corresponding **Init Automatically** attribute or option for the operation. |

## Typical use

Select a public key and verification mechanism, provide the signed input and signature, configure parameters, and run Verify.

## Notes

Use the selected slot and session shown in **Slot Info**. Results depend on the PKCS #11 module, token support, object permissions, and entered values. CryptokiMan and/or the module reports operation errors.

## Source files

- `verify_dlg.ui` defines the dialog layout and visible controls.
- `verify_dlg.cpp` implements dialog behavior and Cryptoki operations.
- `verify_dlg.h` declares the dialog class and interface.
