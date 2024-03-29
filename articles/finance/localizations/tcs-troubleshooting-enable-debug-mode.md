---
title: Den Debug-Modus im Steuerberechnungsdienst aktivieren
description: In diesem Artikel wird erläutert, wie Sie den Debugmodus im Steuerberechnungsdienst aktivieren, um Probleme zu untersuchen.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 2bb381939ebe32cb51caf730cdd441557d83a4c0
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2022
ms.locfileid: "9620897"
---
# <a name="enable-debug-mode-in-the-tax-calculation-service"></a>Den Debug-Modus im Steuerberechnungsdienst aktivieren

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie den Debugmodus im Steuerberechnungsdienst aktivieren, um Probleme zu untersuchen.

1. Fügen Sie **&debug=vs%2CconfirmExit&** zur URL des Anwendungsobjektservers (AOS) hinzu und aktualisieren Sie dann die Seite.
2. Wenn Sie **Mehrwertsteuer** auswählen, um die Mehrwertsteuer zu berechnen, wird eine Textdatei mit dem Namen **TaxServiceTroubleshootingLog.txt** geöffnet. Die Datei **TaxServiceTroubleshootingLog.txt** enthält **TaxableDocument** und die Berechnungsparameter. Diese Ergebnisse werden vom Steuerdienst und Ausnahmeinformationen zur Problembehandlung zurückgegeben.

## <a name="sample"></a>Beispiel

```json
===============================Tax service calculation input JSON:=====================================
{
    "TaxableDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Transaction Line ID": "5816,68719677391",
            ...
            }
        ],
        "Transaction Header ID": "2022,68719506302",
        ...
        }
    ]
    },
    "Parameter": {
    "ContinueOnErrors": true,
    ...
    },
    "Adjustment": {
    "Lines": {}
    }
}
===========================Tax service calculation result JSON:=================================
{
    "taxDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Tax Codes": {
                ...
            }
        ],
        "Measures": {
            "List Code": "EUTrade"
        },
        "Tax Registration ID": null,
        "Transaction Header ID": "2022,68719506302",
        "Errors": null
        }
    ]
    },
    "solutionId": "b51e0025-cbbe-4d37-bf0b-90d7be4f214d|1",
    "isPartialSuccess": false
}
=============================CorrelationId:==============================
"21f3a8a1-ee9a-477b-b44e-b8ec79e74d16"
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
