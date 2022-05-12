---
title: Es wurde kein übereinstimmendes Ergebnis gefunden
description: In diesem Thema wird erklärt, wie Sie den Fehler „Es wurde kein übereinstimmendes Ergebnis gefunden“ im Steuerberechnungsdienst beheben können.
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
ms.openlocfilehash: c1a343b0b74645d40b0a2582749968cc0a56afd7
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645416"
---
# <a name="no-matching-result-could-be-found"></a>Es wurde kein übereinstimmendes Ergebnis gefunden

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Schritte zur Problembehandlung erklärt, die Sie nehmen können, wenn Sie den Fehler „Es wurde kein übereinstimmendes Ergebnis gefunden“ im Steuerberechnungsdienst erhalten.

## <a name="symptom"></a>Symptom

Sie erhalten die folgende Fehlermeldung: „Kopfzeile/Positionen - 1, Steuergruppe, es wurde kein übereinstimmendes Ergebnis gefunden.“

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
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
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

Das Problem tritt auf, wenn die Funktionseinrichtung im Regulatory Configuration Service (RCS) falsch ist.

## <a name="troubleshoot"></a>Problembehandlung

1. Laden Sie die Problembehebungsdatei herunter. Weitere Informationen finden Sie unter [Debugmodus für Problembehandlung aktivieren](tcs-troubleshooting-enable-debug-mode.md).
2. Vergleichen Sie die Eingabe für die Steuerdienstberechnung mit der Funktionseinrichtung, um das Einrichtungsproblem zu beheben.

    Das folgende Beispiel zeigt die Eingabe für die Steuerdienstberechnung.

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    Die folgende Tabelle listet die Steuergruppenanwendbarkeit in RCS auf.

    | Kopfzeile.Geschäftsprozess | Positionen.Unternehmenseinheit | Kopfzeile.Versand von Postleitzahl | MwSt.-Gruppe |
    |-------------------------|---------------------|---------------------------|-----------|
    | Journal                 |                     |                           | Gruppe A   |
    | Vertrieb                   |                     | 30160                     | Gruppe B   |

    Gemäß der Eingabe für die Steuerdienstberechnung ist der Wert **Geschäftsprozess** in der Kopfzeile **Vertrieb** und der Wert **Versand von Postleitzahl** in der Kopfzeile ist **30159**. Diese Eingabe basiert auf der Einrichtung von Anwendbarkeitsregeln in RCS. Da keine übereinstimmende Position vorhanden ist, tritt der Fehler auf.

    > [!NOTE]
    > Wenn der Wert in der Anwendbarkeitsregel leer ist, gilt die Regel für jeden Wert.

## <a name="mitigation"></a>Mitigation

Gehen Sie folgendermaßen vor, um den Fehler zu beheben.

1. Gehen Sie zu RCS zu **Globalisierungsfunktionen** \> **Steuerberechnung**.
2. Erstellen Sie eine neue Version der Funktion.
3. Fügen Sie eine Position für die entsprechenden Informationen hinzu.

    | Kopfzeile.Geschäftsprozess | Positionen.Unternehmenseinheit | Kopfzeile.Versand von Postleitzahl| MwSt.-Gruppe |
    |-------------------------|---------------------|--------------------------|-----------|
    | Journal                 |                     |                          | Gruppe A   |
    | Vertrieb                   |                     | 30160                    | Gruppe B   |
    | Vertrieb                   |                     | 30159                    | Gruppe B   |

4. Veröffentlichen Sie die Funktionseinrichtungsversion.
5. Gehen Sie in Microsoft Dynamics 365 Finance zu **Steuern** \> **Einrichtung** \> **Steuerkonfiguration** \> **Steuerberechnungsparameter** und wählen Sie die neue Version aus.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
