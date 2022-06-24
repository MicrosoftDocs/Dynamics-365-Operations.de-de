---
title: Mehrwertsteuer-Ausgleichsperioden einrichten
description: In diesem Artikel wird erläutert, wie Mehrwertsteuer-Abrechnungszeiträume in Dynamics 365 Finance eingerichtet werden.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f8514494b5d3534fc236def817df0d58fe80d70
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846682"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Mehrwertsteuer-Ausgleichsperioden einrichten

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie Umsatzsteuerverrechnungsperioden einrichten. Mehrwertsteuer-Abrechnungszeiträume enthalten Informationen über die Periodenintervalle für die die Mehrwertsteuer gemeldet und abgeführt werden muss. Ein Abrechnungsprozess kann für einen Abrechnungszeitraum für ein bestimmtes Datumsintervall ausgeführt werden. Alle Steuercodes, die dem Abrechnungszeitraum zugeordnet sind, werden ausgeglichen. Je nach den Einstellungen der zugehörigen "Mehrwertsteuerbehörde", werden die Steuerverbindlichkeiten entweder zu einem Kreditor oder auf ein "Hauptbuchkonto" gebucht.

Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu **Steuer > Indirekte Steuern > Mehrwertsteuer > Mehrwertsteuer-Abrechnungszeiträume**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Abrechnungszeitraum** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Wählen Sie im Feld **Berechtigung** die Umsatzsteuerbehörde, die die Berichte und die Zahlungen erhält, die für den Abrechnungszeitraum angelegt werden.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Wählen Sie im Feld **Zahlungsbedingungen** den gewünschten Datensatz im Dropdown-Menü aus. Die zugehörige Mehrwertsteuerbehörde kann als Kreditor eingerichtet werden und die "Mehrwertsteuerabrechnung" erstellt eine offene Kreditorenrechnung. Die "Zahlungsbedingungen" definieren das "Fälligkeitsdatum" für die offene Kreditorenrechnung.  
8. Wählen Sie einen Typ für die Abrechnungszeitraumintervalle aus.
9. Geben Sie die Anzahl der Periodenintervalleinheiten pro Periode ein. So verfügt beispielsweise ein Quartal über 3 Monate.
10. Aktivieren oder deaktivieren Sie das Kontrollkästchen **Batchverarbeitung für Umsatzsteuerabrechnung verwenden**. Der Abrechnungsprozess für den Abrechnungszeitraum kann als Batchauftrag im Hintergrund verarbeitet werden. Das wird für eine große Zahl von Steuertransaktionen innerhalb eines Periodenintervalls empfohlen.
11. Aktivieren oder deaktivieren Sie das Kontrollkästchen **Verrechnung von Steuertransaktionen verhindern**. Standardmäßig generiert das System Offsetsteuerbuchungen während des Ausgleichsprozesses, die  Performanceprobleme verursachen können,  wenn es viele Steuerbuchungen innerhalb eines Periodenintervalls gibt. Aktivieren bzw. deaktivieren Sie dieses Kontrollkästchen, um Steuerausgleichsbuchungen erstellen zu verhindern.
12. Erweitern Sie die Registerkarte **Periodenintervalle**.
13. Wählen Sie **Hinzufügen** aus.
14. Geben Sie in der neuen Zeile im Feld **Ab Datum** ein Datum ein.
15. Geben Sie im Feld **Bis Datum** ein Datum ein.
16. Wählen Sie **Neues Periodenintervall**. Sobald das erste Periodenintervall eingegeben wurde, können neue Perioden automatisch erstellt werden. Sie können nach Bedarf zurückkehren und neue Periodenintervalle hinzufügen.  
17. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
