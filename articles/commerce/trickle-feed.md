---
title: Auftragserstellung per Einzelzulauf bei Transaktionen im Geschäft
description: In diesem Thema wird die Auftragserstellung per Einzelzulauf für Geschäftstransaktionen in Microsoft Dynamics 365 Commerce beschrieben.
author: analpert
ms.date: 12/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3a7fd8698d7123403cf9092a4a4bf810595d795b
ms.sourcegitcommit: f82372b1e9bf67d055fd265b68ee6d0d2f10d533
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7921244"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Auftragserstellung per Einzelzulauf bei Transaktionen im Geschäft

[!include [banner](includes/banner.md)]

In Microsoft Dynamics 365 Commerce ab Version 10.0.5 wird empfohlen, alle Auszugsbuchungsprozesse auf Einzelzulaufbuchungsprozesse umzustellen. Mit der Verwendung der Einzelzulaufsfunktionalität sind erhebliche Leistungs- und Geschäftsvorteile verbunden. Verkaufstransaktionen werden den ganzen Tag über bearbeitet. Zahlungsmittel- und Bargeldverwaltungstransaktionen werden am Ende des Tages in der Finanzaufstellung verarbeitet. Die Einzelzulaufsfunktionalität ermöglicht die kontinuierliche Verarbeitung von Kundenaufträgen, Rechnungen und Zahlungen. Daher können Bestand, Umsatz und Zahlungen nahezu in Echtzeit aktualisiert und erfasst werden.

## <a name="use-trickle-feed-based-posting"></a>Einzelzulaufbuchung verwenden

> [!IMPORTANT]
> Bevor Sie die Einzelzulaufbuchung aktivieren, müssen Sie sicherstellen, dass keine berechneten und ungebuchten Aufstellungen vorhanden sind. Buchen Sie alle Aufstellungen, bevor Sie die Funktion aktivieren. Sie können im Arbeitsbereich **Finanzdaten für Shop** nach offenen Aufstellungen suchen.

Um die Buchung auf Basis von Einzelzuläufen für Einzelhandelstransaktionen zu aktivieren, aktivieren Sie die Funktion **Einzelhandelsaufstellungen – Einzelzulauf** über den Arbeitsbereich **Funktionsverwaltung**. Aufstellungen werden in zwei Typen unterteilt: Transaktionsaufstellung und Finanzaufstellung.

### <a name="transactional-statements"></a>Buchungsaufstellungen

Die Verarbeitung der Buchungsaufstellungen sollte häufig im Laufe des Tages ausgeführt werden, sodass Dokumente erstellt werden, wenn die Transaktionen in die Commerce-Zentralverwaltung hochgeladen werden. Die Buchungen werden aus den Shops in die Commerce-Zentralverwaltung geladen, wenn Sie den **P-Auftrag** ausführen. Sie müssen auch den Einzelvorgang **Geschäftsbuchungen überprüfen** ausführen, um Transaktionen zu prüfen, damit die Transaktionsaufstellung sie aufnimmt.

Planen Sie die folgenden Einzelvorgänge so, dass sie mit großer Häufigkeit ausgeführt werden:

- Um eine Transaktionsaufstellung zu berechnen, führen Sie den Einzelvorgang **Transaktionsaufstellungen stapelweise berechnen** aus (**Retail und Commerce \> Retail und Commerce IT \> POS-Buchung \> Transaktionsaufstellungen stapelweise berechnen**). Dieser Einzelvorgang ruft alle nicht gebuchten und geprüften Transaktionen ab und fügt sie einer neuen Transaktionsaufstellung hinzu.
- Um Transaktionsaufstellungen stapelweise zu buchen, führen Sie den Einzelvorgang **Transaktionsaufstellungen stapelweise buchen** aus (**Retail und Commerce \> Retail und Commerce IT \> POS-Buchung \> Transaktionsaufstellungen stapelweise buchen**). Dieser Einzelvorgang führt den Buchungsprozess aus und erstellt Verkaufsaufträge, Verkaufsrechnungen, Zahlungserfassungen, Rabatterfassungen und Einnahmen-Ausgaben-Buchungen für noch nicht gebuchte Aufstellungen, die keine Fehler enthalten. 

### <a name="financial-statements"></a>Finanzaufstellungen

Die Verarbeitung der Finanzaufstellungen sollte am Ende des Tages erfolgen. Diese Art der Aufstellungsverarbeitung unterstützt nur die **Schicht**-Abschlussmethode und nimmt nur abgeschlossene Schichten auf. Die Aufstellungen beschränken sich auf Finanzabstimmung. Sie erstellen nur die Erfassungen zu den Differenzbeträgen zwischen gezähltem Betrag und Transaktionsbetrag für die verschiedenen Zahlungsmittel sowie Erfassungen zu anderen Bargeldverwaltungstransaktionen.

Planen Sie die Start- und Endzeiten der folgenden Finanzaufstellungen basierend auf dem erwarteten Tagesende:

- Um eine Finanzaufstellung zu berechnen, führen Sie den Einzelvorgang **Finanzaufstellungen stapelweise berechnen** aus (**Retail und Commerce \> Retail und Commerce IT \> POS-Buchung \> Finanzaufstellungen stapelweise berechnen**). Dieser Einzelvorgang erfasst alle nicht gebuchten Finanztransaktionen und fügt sie einer neuen Finanzaufstellung hinzu.
- Um eine Finanzaufstellung stapelweise zu buchen, führen Sie den Einzelvorgang **Finanzaufstellungen stapelweise buchen** aus (**Retail und Commerce \> Retail und Commerce IT \> POS-Buchung \> Finanzaufstellungen stapelweise buchen**).

### <a name="manually-create-statements"></a>Aufstellungen manuell erstellen

Transaktions- und Finanzaufstellungen können auch manuell erstellt werden. 

1. Wechseln Sie zu **Retail und Commerce \> Kanäle \> Shops**, und klicken Sie auf **Aufstellungen**. 
2. Wählen Sie **Neu** und dann den zu erstellenden Aufstellungstyp aus. Felder auf der Seite **Aufstellungen** zeigen relevante Daten für den Aufstellungstyp und die Aktionen unter der Gruppe **Aufstellung** zeigen relevante Aktionen an.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
