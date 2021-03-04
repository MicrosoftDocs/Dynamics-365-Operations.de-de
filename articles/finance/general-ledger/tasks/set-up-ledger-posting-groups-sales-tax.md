---
title: Sachkontobuchungsgruppen für Mehrwertsteuer einrichten
description: Die Mehrwertsteuer wird zu den Hauptkonten berechnet und gebucht, die in den „Sachkontobuchungsgruppen“ angegeben werden.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90fe7f3ab08e9417af3f857f04934a9b5df3d82d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644896"
---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Sachkontobuchungsgruppen für Mehrwertsteuer einrichten

[!include [banner](../../includes/banner.md)]

Die Mehrwertsteuer wird zu den Hauptkonten berechnet und gebucht, die in den „Sachkontobuchungsgruppen“ angegeben werden. Sachkontobuchungsgruppen werden jedem einzelnen Mehrwertsteuercode zugeordnet. Sie können einzelne Sachkontobuchungsgruppen für jeden Mehrwertsteuercode einrichten, eine Sachkontobuchungsgruppe für alle Mehrwertsteuercodes verwenden oder mehrere Sachkontobuchungsgruppen den Mehrwertsteuercodes zuweisen. Für diese Erfassung wird das Demo-Unternehmen DEMF verwendet. 

1. Gehen Sie zu **Navigationsbereich > Module > Steuer > Einrichtung > Umsatzsteuer > Kontenbuchungsgruppen**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Kontenbuchungsgruppe** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Wählen Sie im Feld **Verkaufssteuerverbindlichkeiten** das Hauptkonto für ausgehende Umsatzsteuern, die an die Steuerbehörde zu zahlen sind. Mehrwertsteuern werden im Namen der Steuerbehörde erhoben, wenn Sie steuerpflichtige Waren und Dienstleistungen verkaufen.  
6. Wählen Sie im Feld **Verkaufsforderung** das Hauptkonto für eingehende Steuern, die von der Steuerbehörde erhalten werden. Händler erheben Steuern im Auftrag der Steuerbehörde, wenn Sie steuerpflichtige Waren und Dienstleistungen kaufen. Dieses Feld ist nicht verfügbar, wenn auf der Seite **Hauptbuchparameter** die Option Umsatzsteuerregeln anwenden markiert ist. Stattdessen werden an Händler gezahlte Mehrwertsteuerbeträge vom selben Konto abgebucht, wie der Einkauf.   
7. Wählen Sie im Feld **Steueraufwand verwenden** das Hauptkonto für die Buchung von abzugsfähigen Nutzungssteuern, die von den Verkäufern im Rahmen der EU-Reversion GST/HST nicht in Anspruch genommen oder an die Steuerbehörde gemeldet werden. Die Option **Steuer verwenden** muss für das **Verkaufssteuerkennzeichen** im **Verkaufssteuerkennzeichen** ausgewählt werden, das in der Transaktion verwendet wird. Dieses Feld ist nicht verfügbar, wenn auf der Seite **Hauptbuchparameter** die Option **Umsatzsteuerregeln anwenden** markiert ist.   
8. Wählen Sie im Feld **Verwendung der Steuerverbindlichkeiten** das Hauptkonto für die Buchung eingehender Verwendungssteuern, die an die Steuerbehörden zu zahlen sind. Die Option **Steuer verwenden** muss in der Option **Umsatzsteuerkennzeichen** in der Option **Umsatzsteuerkennzeichen** ausgewählt sein, um **Steuer verwenden** zu buchen. Wenn auf der Seite **Hauptbuchparameter** die Option **Verkaufssteuerregeln anwenden** ausgewählt ist, wird der Ausgleich auf das Aufwandskonto des Geschäfts gebucht.   
9. Wählen Sie im Feld **Verrechnungskonto** das Hauptkonto aus, auf das der Nettosaldo der in den Feldern **Verwendungssteuerverbindlichkeiten** und **Verkaufssteuerforderungen** angegebenen Sachkonten gebucht werden soll. Der Saldo wird bei Ausführung der Umsatzsteuerabrechnung und des Buchungseinzelvorgangs erstellt.  Wenn die Steuerbehörde für den Abrechnungszeitraum einem Kreditorenkonto zugeordnet ist, wird der Saldo stattdessen auf das Kreditorenkonto gebucht.
10. Wählen Sie im Feld **Lieferant Skonto** das Hauptkonto zum Buchen von Skonto für Umsatzsteuerkennzeichen, die dieser Ledger-Buchungsgruppe zugeordnet sind. Dies ist optional und wenn kein Konto eingegeben wird, wird das Hauptkonto unter **Skontoabzugscodes** verwendet. Es kann sinnvoll sein, unterschiedliche Konten pro **Ledger-Buchungsgruppe** zu verwenden, wenn Sie die Option Umsatzsteuer auf Skonto umgekehrt auf Umsatzsteuergruppen verwenden.  
11. Wählen Sie im Feld **Kundenfallrabatt** das Hauptkonto zum Buchen von Skonto für **Verkaufssteuerkennzeichen**, das dieser **Sachkonto-Buchungsgruppe** zugeordnet ist. Dies ist optional und wenn kein Konto eingegeben wird, wird das Hauptkonto auf den **Skontoabzugscodes** verwendet. Es kann sinnvoll sein, unterschiedliche Konten pro **Sachkonto-Buchungsgruppe** zu verwenden, wenn Sie die Option Umsatzsteuer auf Skonto auf **Verkaufssteuergruppen** verwenden.  
12. Klicken Sie auf **Speichern**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]