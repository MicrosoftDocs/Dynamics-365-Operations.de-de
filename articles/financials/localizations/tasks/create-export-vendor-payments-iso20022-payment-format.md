--- 
title: Kreditorenzahlungen mithilfe eines ISO20022-Zahlungsformats erstellen und exportieren
description: "Diese Prozedur zeigt, wie Sie Zahlungspositionen in der Kreditorzahlungserfassung erstellen und eine Kreditorenzahlungsdatei über die ISO2022 Kreditübertragung erstellen."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Kreditorenzahlungen mithilfe eines ISO20022-Zahlungsformats erstellen und exportieren

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie Sie Zahlungspositionen in der Kreditorzahlungserfassung erstellen und eine Kreditorenzahlungsdatei über die ISO2022 Kreditübertragung erstellen. 

Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DEMF.

Dies ist der fünfte von fünf Aufgaben, die das Verfahren für Kreditorenzahlung über elektronischen Berichterstellungskonfigurationen zeigen. Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.


## <a name="create-payment-lines"></a>Zahlungspositionen erstellen
1. Wechseln Sie zu "Kreditoren" > "Zahlungen" > "Zahlungserfassung".
2. Klicken Sie auf "Neu".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.
5. Klicken Sie auf "Positionen".
6. Klicken Sie auf "Zahlungsvorschlag".
7. Klicken Sie auf "Zahlungsvorschlag erstellen".
8. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
9. Klicken Sie auf "Filter".
10. In der Liste wählen Sie die Zeile für Tabelle und das Feld "Kreditorenkonto" aus.
11. Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.
    * Sie können alle beliebigen Kriterien für die Auswahl von Kreditorenbuchungen anwenden. In diesem Beispiel verwenden Sie DE-001 als Kreditorenkonto.  
12. Klicken Sie auf "OK".
13. Klicken Sie auf "OK".
14. Klicken Sie auf "Zahlungen erstellen".

## <a name="generate-an-iso20022-payment-file"></a>ISO20022-Zahlungsdatei generieren


