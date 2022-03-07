---
title: Auftragserstellung per Einzelzulauf bei Transaktionen im Geschäft
description: In diesem Thema wird die Auftragserstellung per Einzelzulauf für Geschäftstransaktionen in Microsoft Dynamics 365 Commerce beschrieben.
author: analpert
ms.date: 01/11/2021
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
ms.openlocfilehash: 67b66cd4bf2a77f3ab7f33f691156e38cc13770a
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964628"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Auftragserstellung per Einzelzulauf bei Transaktionen im Geschäft

[!include [banner](includes/banner.md)]

In Microsoft Dynamics 365 Commerce ab Version 10.0.5 wird empfohlen, alle Auszugsbuchungsprozesse auf Einzelzulaufbuchungsprozesse umzustellen. Mit der Verwendung der Einzelzulaufsfunktionalität sind erhebliche Leistungs- und Geschäftsvorteile verbunden. Verkaufstransaktionen werden den ganzen Tag über bearbeitet. Zahlungsmittel- und Bargeldverwaltungstransaktionen werden am Ende des Tages in der Finanzaufstellung verarbeitet. Der Einzelzulauf ermöglicht eine kontinuierliche Bearbeitung von Kundenaufträgen, Rechnungen und Zahlungen. Daher können Bestand, Umsatz und Zahlungen nahezu in Echtzeit aktualisiert und erfasst werden.

## <a name="use-trickle-feed-based-posting"></a>Einzelzulaufbuchung verwenden

> [!IMPORTANT]
> Bevor Sie die Einzelzulaufbuchung aktivieren, müssen Sie sicherstellen, dass keine berechneten und ungebuchten Aufstellungen vorhanden sind. Buchen Sie alle Aufstellungen, bevor Sie die Funktion aktivieren. Sie können im Arbeitsbereich **Finanzdaten für Shop** nach offenen Aufstellungen suchen.

Um die Buchung auf Basis von Einzelzuläufen für Einzelhandelstransaktionen zu aktivieren, aktivieren Sie die Funktion **Einzelhandelsaufstellungen – Einzelzulauf** über den Arbeitsbereich **Funktionsverwaltung**. Aufstellungen werden in zwei Typen unterteilt: Transaktionsaufstellung und Finanzaufstellung.

### <a name="transactional-statements"></a>Buchungsaufstellungen

Die Verarbeitung von Buchungsaufstellungen soll oft im Laufe des Tages ausgeführt werden, damit Dokumente dann erstellt werden, wenn die Buchungen in die Commerce-Zentralverwaltung hochgeladen werden. Die Buchungen werden aus den Shops in die Commerce-Zentralverwaltung geladen, wenn Sie den **P-Auftrag** ausführen. Sie müssen auch den Einzelvorgang **Geschäftsbuchungen überprüfen** ausführen, um Transaktionen zu prüfen, damit die Transaktionsaufstellung sie aufnimmt.

Planen Sie die folgenden Einzelvorgänge so, dass sie mit großer Häufigkeit ausgeführt werden:

- Um eine Transaktionsaufstellung zu berechnen, führen Sie den Einzelvorgang **Transaktionsaufstellungen stapelweise berechnen** aus (**Retail und Commerce \> Retail und Commerce IT \> POS-Buchung \> Transaktionsaufstellungen stapelweise berechnen**). Dieser Einzelvorgang ruft alle nicht gebuchten und geprüften Transaktionen ab und fügt sie einer neuen Transaktionsaufstellung hinzu.
- Um Transaktionsaufstellungen stapelweise zu buchen, führen Sie den Einzelvorgang **Transaktionsaufstellungen stapelweise buchen** aus (**Retail und Commerce \> Retail und Commerce IT \> POS-Buchung \> Transaktionsaufstellungen stapelweise buchen**). Dieser Einzelvorgang führt den Buchungsprozess aus und erstellt Verkaufsaufträge, Verkaufsrechnungen, Zahlungserfassungen, Rabatterfassungen und Einnahmen-Ausgaben-Buchungen für noch nicht gebuchte Aufstellungen, die keine Fehler enthalten. 

### <a name="financial-statements"></a>Finanzaufstellungen

Die Verarbeitung der Finanzaufstellungen sollte am Ende des Tages erfolgen. Diese Art der Aufstellungsverarbeitung unterstützt nur die **Schicht**-Abschlussmethode und nimmt nur abgeschlossene Schichten auf. Die Aufstellungen beschränken sich auf Finanzabstimmung. Sie erstellen nur die Erfassungen zu den Differenzbeträgen zwischen gezähltem Betrag und Transaktionsbetrag bei den verschiedenen Zahlungsmitteln sowie Erfassungen zu anderen Bargeldverwaltungstransaktionen.

Finanzaufstellungen erlauben auch die Prüfung folgender Transaktionen: Transaktionen zur Zahlungsmitteldeklaration, Zahlungstransaktionen, Zahlungsmitteltransaktionen und sichere Zahlungsmitteltransaktionen. Die Seite mit den Einzelheiten zu Zahlungsmitteln wird nur bei Auswahl einer Finanzaufstellung angezeigt.

![Das Bild zeigt den Abschnitt mit den Einzelheiten zu Zahlungsmitteln auf dem Formular für gebuchte Aufstellungen bei Auswahl einer Finanzaufstellung.](./media/Trickle-feed-posted-statements-transaction-view.png)

Planen Sie die Start- und Endzeiten der folgenden Finanzaufstellungen entsprechend dem erwarteten Tagesende:

- Um eine Finanzaufstellung zu berechnen, führen Sie den Einzelvorgang **Finanzaufstellungen stapelweise berechnen** aus (**Retail und Commerce \> Retail und Commerce IT \> POS-Buchung \> Finanzaufstellungen stapelweise berechnen**). Dieser Einzelvorgang erfasst alle nicht gebuchten Finanztransaktionen und fügt sie einer neuen Finanzaufstellung hinzu.
- Um eine Finanzaufstellung stapelweise zu buchen, führen Sie den Einzelvorgang **Finanzaufstellungen stapelweise buchen** aus (**Retail und Commerce \> Retail und Commerce IT \> POS-Buchung \> Finanzaufstellungen stapelweise buchen**).

### <a name="manually-create-statements"></a>Aufstellungen manuell erstellen

Transaktions- und Finanzaufstellungen können auch manuell erstellt werden. 

1. Wechseln Sie zu **Retail und Commerce \> Kanäle \> Shops**, und klicken Sie auf **Aufstellungen**. 
2. Wählen Sie **Neu** und dann den zu erstellenden Aufstellungstyp aus. Felder auf der Seite **Aufstellungen** zeigen relevante Daten für den Aufstellungstyp und die Aktionen unter der Gruppe **Aufstellung** zeigen relevante Aktionen an.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
