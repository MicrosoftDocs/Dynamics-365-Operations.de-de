--- 
title: Mehrwertsteuer-Ausgleichsperioden einrichten
description: "Mehrwertsteuer-Abrechnungszeiträume enthalten Informationen über die Periodenintervalle für die die Mehrwertsteuer gemeldet und abgeführt werden muss."
author: twheeloc
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: ab7d3a00a327f42a9f70c954d9b64a360a7f9163
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-tax-settlement-periods"></a>Mehrwertsteuer-Ausgleichsperioden einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Mehrwertsteuer-Abrechnungszeiträume enthalten Informationen über die Periodenintervalle für die die Mehrwertsteuer gemeldet und abgeführt werden muss. Ein Abrechnungsprozess kann für einen Abrechnungszeitraum für ein bestimmtes Datumsintervall ausgeführt werden. Alle Steuercodes, die dem Abrechnungszeitraum zugeordnet sind, werden ausgeglichen. Je nach den Einstellungen der zugehörigen "Mehrwertsteuerbehörde", werden die Steuerverbindlichkeiten entweder zu einem Kreditor oder auf ein "Hauptbuchkonto" gebucht.



Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.



1. Wechseln Sie zu "Steuer" Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Mehrwertsteuer-Abrechnungszeiträume".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Abrechnungszeitraum" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie im Feld "Behörde" die Mehrwertsteuerbehörde aus, die der Empfänger der Berichte und der Zahlungen in Verbindung mit dem Abrechnungszeitraum ist.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie im Feld "Zahlungsbedingungen" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die zugehörige Mehrwertsteuerbehörde kann als Kreditor eingerichtet werden und die "Mehrwertsteuerabrechnung" erstellt eine offene Kreditorenrechnung. Die "Zahlungsbedingungen" definieren das "Fälligkeitsdatum" für die offene Kreditorenrechnung.  
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
10. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
11. Wählen Sie einen Typ für die Abrechnungszeitraumintervalle aus.
12. Geben Sie die Anzahl der Periodenintervalleinheiten pro Periode ein. So verfügt beispielsweise ein Quartal über 3 Monate.
13. Aktivieren oder deaktivieren Sie das Kontrollkästchen "Stapelverarbeitung für die Mehrwertsteuerabrechnung verwenden".
    * Der Abrechnungsprozess für den Abrechnungszeitraum kann als Batchauftrag im Hintergrund verarbeitet werden. Das wird für eine große Zahl von Steuertransaktionen innerhalb eines Periodenintervalls empfohlen.  
14. Erweitern Sie die Registerkarte "Periodenintervalle".
15. Klicken Sie auf Hinzufügen.
16. Markieren Sie in der Liste die ausgewählte Zeile.
17. Geben Sie in das Feld "Von Datum" ein Datum ein.
18. Geben Sie in das Feld "Bis Datum" ein Datum ein.
19. Klicken Sie auf "Neues Periodenintervall".
    * Sobald das erste Periodenintervall eingegeben wurde, können neue Perioden automatisch erstellt werden. Sie können nach Bedarf zurückkehren und neue Periodenintervalle hinzufügen.  
20. Schließen Sie die Seite.


