---
title: Steuercode kann nicht ermittelt werden
description: In diesem Artikel wird erklärt, wie Sie den Fehler „Steuercode kann nicht bestimmt werden“ im Steuerberechnungsdienst beheben können.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 6a74724de38cf362900277ab9addc8e6894f7689
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877858"
---
# <a name="tax-code-cannot-be-determined"></a>Steuercode kann nicht ermittelt werden

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Schritte zur Problembehandlung erklärt, die Sie nehmen können, wenn Sie den Fehler „Steuercode kann nicht bestimmt werden“ im Steuerberechnungsdienst erhalten.

## <a name="symptom"></a>Symptom

Sie erhalten folgende Fehlermeldung: „Kopfzeile/Positionen - 1, Steuercode kann nicht bestimmt werden.“ Alternativ finden Sie den Fehler in der Problembehebungsdatei, wie im folgenden Beispiel gezeigt. Weitere Informationen finden Sie unter [Debugmodus für Problembehandlung aktivieren](tcs-troubleshooting-enable-debug-mode.md).

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Ursache

Das Problem tritt wahrscheinlich auf, weil sich die Steuergruppe und die Artikelsteuergruppe nicht überschneiden.

## <a name="troubleshoot"></a>Problembehandlung

Führen Sie die folgenden Schritte aus, um das Problem zu beheben.

1. Überprüfen Sie in der Problembehebungsdatei, ob die Steuergruppe und die Artikelsteuergruppe ermittelt wurden. Wenn die Werte für **Steuergruppe** und **Artikelsteuergruppe** leer sind, wurden die Steuergruppe und die Artikelsteuergruppe nicht bestimmt. Wenn sie bestimmt wurden, können die Ergebnisse falsch sein.

    Es folgt das Beispiel einer Problembehebungsdatei.

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
                            "Adjustment": null
                        }
                    ],
                    "Measures": {
                        ...
                    },
                    ...
                }
            ]
        },
        ...
    }
    ```

2. Überprüfen Sie, ob die Option **Mehrwertsteuerüberschreibung** auf der Registerkarte **Einrichtung** der Auftragspositionsdetails aktiviert ist.

    - Wenn sie aktiviert ist, werden die Steuercodes von den Werten **Steuergruppe** und **Artikelsteuergruppe** bestimmt, die Sie in die Buchungsposition eingeben. Überprüfen Sie, ob diese Werte korrekt eingegeben wurden.
    - Wenn sie nicht aktiviert ist, überprüfen Sie, ob die richtigen Werte für die Felder **Anwendbarkeit der Steuergruppe** und **Anwendbarkeit der Artikelsteuergruppe** festgelegt wurden. Weitere Informationen finden Sie unter [Es wurden keine übereinstimmenden Ergebnisse gefunden](tcs-troubleshooting-no-matching-result.md).

3. Wenn die Steuergruppe und die Artikelsteuergruppe korrekt ermittelt wurden, ermitteln Sie, ob es für sie eine Schnittmenge gibt.

    1. Gehen Sie in RCS zu **Steuerfunktionen** \> **Steuercodes und ‑gruppen** \> **Steuergruppe**.

        | Position.Steuergruppe | Steuercodes |
        |----------------|-----------|
        | Gruppe A        | K         |

    2. Gehen Sie zu **Steuerfunktionen** \> **Steuercodes und ‑gruppen** \> **Artikelsteuergruppe**.

        | Position.Artikelsteuergruppe | Steuercodes |
        |---------------------|-----------|
        | Gruppe B             | Mrd         |

    Wenn es keine Schnittmenge für die Steuergruppe und die Artikelsteuergruppe gibt, wird der Steuercode nicht ermittelt.

## <a name="mitigation"></a>Mitigation

1. Führen Sie jeden Schritt im Abschnitt [Problembehandlung](#troubleshoot) dieses Artikels durch und korrigieren Sie die Einrichtung nach Bedarf. Wenn die Steuergruppe und die Artikelsteuergruppe nicht korrekt ermittelt wurden, lesen Sie [Es wurden keine übereinstimmenden Ergebnisse gefunden](tcs-troubleshooting-no-matching-result.md).
2. Wenn es keine Schnittmenge für die Steuergruppe und die Artikelsteuergruppe gibt, erstellen Sie eine neue Funktionsversion in RCS und korrigieren Sie die Einrichtung.

    - Gehen Sie zu **Steuerfunktionen** \> **Steuercodes und ‑gruppen** > **Artikelsteuergruppe**.

        | Position.Artikelsteuergruppe | Steuercodes |
        |---------------------|-----------|
        | Gruppe B             | A;B       |

    Der Steuercode wird als **A** ermittelt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
