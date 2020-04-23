---
title: " Konfigurationen für Einzelhandelsauszüge speichern"
description: Diese Prozedur zeigt Schritt für Schritt Konfigurationen für den Shop, die sich darauf auswirken, wie Commerce-Auszüge erstellt und gebucht werden.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57081b9e737373641cd9d884919d03dcf62a2ffe
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140654"
---
# <a name="store-configurations-for-retail-statements"></a> Konfigurationen für Einzelhandelsauszüge speichern

[!include [banner](../includes/banner.md)]

Diese Prozedur zeigt Schritt für Schritt Konfigurationen für den Shop, die sich darauf auswirken, wie Commerce-Auszüge erstellt und gebucht werden. Finanzdimensionen in Shops werden durch eine andere Prozedur abgedeckt. Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.

1. Gehen Sie im **Navigationsbereich** zu **Module > Retail und Commerce > Kanäle > Shops > Alle Shops**.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie auf **Bearbeiten**.
5. Die Einstellungen in der **Auszug/Schließen** fastTab wirken sich auf die Erstellung, Validierung und Buchung von Auszügen für die Filiale aus. Erweitern Sie die **Auszug/Schließen** fastTab.  
6. Wählen Sie im Feld **Auszugsmethode** die Methode aus, mit der Sie die Auszugszeilen gruppieren möchten.  
7. Wählen Sie „Ja“ unter **Ein Auszug pro Tag**, wenn bei der Erstellung von Auszügen aus dem Batch-Job der Auszugserstellung nur ein Auszug pro Tag erstellt werden soll.  
8. Das Feld **Kassensturzberechnung** definiert, ob Kassensturzberechnungen addiert werden sollen oder ob die letzte verwendet werden soll.  
9. Wählen Sie im Feld **Rundung** das Sachkonto aus, in das Rundungsdifferenzen gebucht werden sollen.  
10. Geben Sie im Feld **Maximale Rundungsdifferenz** die maximal zulässige Rundungsdifferenz ein.
11. Geben Sie im Feld **Buchung** die maximal zulässige Gesamtbuchungsdifferenz für einen Auszug ein.
12. Geben Sie im Feld **Shift** die maximale Gesamtdifferenz innerhalb einer Schicht in einen Auszug ein.  
13. Geben Sie in das Feld **Transaktion** die maximale Gesamtdifferenz in einer Auszugszeile ein.  
14. Definieren Sie im Feld **Schließmethode**, ob Transaktionen, die in einen Auszug aufgenommen werden, Teil einer geschlossenen Schicht sein sollen oder ob es sich um Transaktionen innerhalb des definierten Datums-/Zeitbereichs handeln kann.  
15. Geben Sie im Feld **Ende des Geschäftstages** eine Uhrzeit ein, wenn Transaktionen, die nach Mitternacht stattfinden, mit dem Vortag gebucht werden sollen.  
16. Wählen Sie „Ja“ unter **Als Geschäftstag buchen**, wenn Transaktionen, die nach Mitternacht stattfinden, als Teil des Vortages gebucht werden sollen.  
17. Wählen Sie „Ja“ unter **Nach Auszugsmethode aufteilen**, um Auszüge für jede definierte Auszugsmethode zu erstellen. Dies kann hilfreich sein, wenn die Leistung der Buchung für Shops mit hohem Buchungsvolumen verbessert werden muss, da viele kleinere Auszüge erstellt werden, die parallel verarbeitet werden können.  
18. Im Feld **Allgemein** fastTab, im Feld **Standardkunde** können Sie das Kundenkonto auswählen, das für den Verkauf an Laufkundschaft verwendet werden soll.  
