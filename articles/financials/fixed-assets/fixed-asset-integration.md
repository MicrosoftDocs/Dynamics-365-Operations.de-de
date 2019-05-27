---
title: Integration von Anlagevermögen
description: Anlagen können in die Module "Hauptbuch", "Bestandsverwaltung", "Debitoren" und "Kreditoren" integriert werden. Darüber hinaus können Anlagen auch für die Integration in Bestellungen eingerichtet werden.
author: ShylaThompson
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3501
ms.assetid: f0639053-d99c-432a-8ead-5c26e0d4eaec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2023d68a1455c6bb5ec569b6ae19fc3268f8769d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545485"
---
# <a name="fixed-assets-integration"></a>Integration von Anlagevermögen

[!include [banner](../includes/banner.md)]

Anlagen können in die Module "Hauptbuch", "Bestandsverwaltung", "Debitoren" und "Kreditoren" integriert werden. Darüber hinaus können Anlagen auch für die Integration in Bestellungen eingerichtet werden.

<a name="general-ledger"></a>Hauptbuch
--------------

Im Hauptbuch wird der Wert des Anlagevermögens normalerweise in mehreren Hauptkonten zusammengefasst, die für Finanzberichte erforderlich sind. Auf der Seite **Analgen** können Sie jedoch viele Anlagendatensätze erstellen. Diese Datensätze können Informationen wie den Anschaffungspreis, die Abschreibung und die Bewertung enthalten. Jedes Mal, wenn Sie einen Posten für eine Anlage buchen, werden die entsprechenden Hauptkonten aktualisiert. In den Hauptkonten für Anlagen wird immer der aktualisierte Wert der Anlagen aufgeführt.

Auf der Seite**Anlagenbuchungsprofile** definieren Sie die Hauptkonten, in denen Wertmodellbuchungen für Anlagen gebucht werden. Darüber hinaus geben Sie die Arten von Anlagenbuchungen an, die in jedem Hauptkonto gebucht werden. Sie können unterschiedliche Kombinationen aus Anlagenhauptkonten erstellen, je nach der Detailebene, die für Anlagen im Hauptbuch gewünscht wird. Hauptkonten können auf Buchungsarten, Büchern und anderen Hauptkonten basieren.

## <a name="inventory-management"></a>Lagerverwaltung
In der Lagererfassung für Anlagen können Sie die Anschaffung von Anlagen eingeben, die die juristische Person für sich erstellt oder erzeugt hat. Sie können dann Lagerartikel entweder als Anschaffung oder als Teil einer Anschaffung an Anlagen übertragen. 

Die Anschaffung von Anlagen kann auch mithilfe von Bestellungen erfolgen. Wenn Bestellungen Lagerartikel enthalten, die als Anlagen festgelegt sind, wird durch die Einstellung der Option **Anlagenanschaffung aus Einkauf zulassen** auf der Seite **Anlagenparameter** bestimmt, ob für die Anlage bei der Buchung der Rechnung eine Anschaffung gebucht wird. Eine Einkaufsposition erstellt eine Anlage, unabhängig von der Menge. Die Auswirkungen, den die Anschaffung von Anlagen auf Lager hat, hängt von der Konfiguration der juristischen Person ab. 

Entwickelt sich ein Lagerartikel zu einer Anlagenanschaffung entweder über die Lagererfassung, eine Bestellung oder einen Anschaffungsvorschlag, wird eine Wertmodellanschaffungsbuchung für die Anlage erstellt. Umfasst eine Wertmodellanschaffung ein abgeleitetes Abschreibungsbuch, wird darüber hinaus im Abschreibungsbuch eine Anschaffungsbuchung erstellt. 

Buchungsregeln, die auf der Seite **Buchung** in der Bestandverwaltung eingerichtet werden, steuern den Bestand, wenn eine Anschaffung gebucht wird. In bestimmten Fällen soll das Lager jedoch möglicherweise nicht verringert werden, nachdem anlagenbezogene Rechnungen gebucht worden sind In einigen Fällen werden die Anlagen zur internen Verwendung eingekauft. Ein Beispiel ist ein Laptop, der für die Verkaufsabteilung eingekauft wird. Bei Verwendung von Bestellungen können Artikel verwendet werden, die sowohl für den Wiederverkauf als auch für die interne Verwendung eingerichtet sind. 

Werden für Artikelgruppen bestimmte Zu- und Abgangskonten für Anlagen verwendet, kann der gleiche Lagerartikel sowohl für interne Einkäufe als auch für Bestand verwendet werden, der für den Wiederverkauf bestimmt ist. 

Anlagen, die für den internen Gebrauch bestimmt sind, werden so eingerichtet, dass sie die Kontenart **Anlagenempfang**" haben. Diese Kontenart wird verwendet, um den Eingang der Anlage nachzuverfolgen. Wenn Sie eine Kreditorenrechnung buchen, verwenden Sie das Anlagenzugangskonto, sofern eine der folgenden Bedingungen zutrifft:

-   Die Rechnungsposition enthält eine vorhandene Anlage zu internen Zwecken.
-   Das Kontrollkästchen **Neue Anlagen** wird für die Produktzugangsposition ausgewählt, die gebucht wird.
-   Das Kontrollkästchen **Neue Anlage erstellen** ist für die Kreditorenrechnungsposition aktiviert.

Dieses Konto ist in der Regel ein Ausgabenkonto. Sie können die Kontenart **Anlagenzugang** entweder für eine Artikelgruppe oder für einen einzelnen Artikel einrichten, indem Sie die Registerkarte **Bestellung** auf den Seiten **Artikelgruppe** oder **Buchung** verwenden.

Ebenso können Anlagen, die für den internen Gebrauch bestimmt sind, so eingerichtet werden, dass sie die Kontenart **Anlagenabgang** haben. Diese Kontenart wird verwendet, um die Ausstellung der Anlage an den Empfänger nachzuverfolgen. Wenn eine Anlage unter Verwendung einer Bestellung angeschafft wurde, fungiert das Anlagenzugangskonto als Gegenkonto zu dem Anlagenabgangskonten. Die Anlagenanschaffung kann entweder gebucht werden, wenn Sie eine Kreditorenrechnung buchen oder wenn Sie die Anlagenanschaffung in der Erfassung "Anlagen" buchen, möglicherweise mithilfe eines Anschaffungsvorschlags. Sie können die Kontenart **Anlagenabgang** entweder für eine Artikelgruppe oder für einen einzelnen Artikel einrichten, indem Sie die Registerkarte **Bestand** auf der Seite **Lagergruppe** oder **Artikelgruppe** verwenden. 

Letztendlich werden die Hauptkonten, die für die Buchung verwendet werden, durch die Optionen für Sachkontenintegration bestimmt, die für die Artikelmodellgruppe angegeben werden. Darüber hinaus variieren die Hauptkonten, die verwendet werden, je nachdem, ob der Bestellposition eine Anlage zugewiesen ist. Die Konten werden vom Buchungsprofil der jeweiligen Artikelgruppe abgeleitet. 
**Hinweis:** Ist beim Buchen von Produktzugängen eine Lagerreservierung vorhanden, ist das Zuweisen einer Anlage sowie das Erstellen einer Anlage auf Basis der Position nicht möglich. 

Die Konten, in denen Anlagenbuchungen erfasst werden, und auch die Buchungsart der Anlage sind von zwei Faktoren abhängig: ob Anlagen von der juristischen Person zugekauft oder selbst errichtet werden. 

Die Buchungsart fungiert als Verknüpfung zwischen der Lagerbuchung und dem Buchungsprofil im Modul "Anlagevermögen". Da durch das Buchungsprofil im Modul "Anlagevermögen" festgelegt wird, welche Konten aktualisiert werden, werden mit der Auswahl der Anlagenbuchungsart indirekt auch die Sachkonten ausgewählt, auf die die Buchung erfolgt. Für selbst erstellte sowie für eingekaufte Anlagen wird in der Regel die Buchungsart **Anschaffung** oder **Anschaffungsänderung** verwendet.

## <a name="accounts-receivable"></a>Debitorenkonten
Zur Integration von Anlagen in Debitoren werden Buchungsprofile verwendet, die im Modul "Anlagevermögen" eingerichtet werden. Diese Buchungsprofile werden aktiviert, wenn vor der Buchung der Debitorenrechnung eine Anlage, ein Wertmodell und eine entsprechende Buchungsart für eine Debitorenrechnung ausgewählt wird. Da Anlagen nicht Teil der "Lagerverwaltung" sind, müssen Sie die Seite **Freitextrechnung** verwenden, wenn Sie eine Anlage verkaufen. 

Wenn das Wertmodell ein abgeleitetes Abschreibungsbuch umfasst, wird beim Buchen der Debitorenrechnung eine Abschreibungsbuchbuchung erstellt.

## <a name="accounts-payable"></a>Kreditorenkonten
Anlagen werden in der Regel von externen Kreditoren erworben. Auf der Seite **Anlagenparameter** können Sie angeben, ob Anlagenanschaffungen immer zusammen mit den Kreditorenrechnungen gebucht werden oder ob Anlagenanschaffungen ausschließlich über "Anlagen" buchbar sein sollen. Um Anschaffungsbuchungen vom Modul "Kreditoren" zuzulassen, werden die Anlagenkonten bei jeder Buchung einer Kreditorenrechnung aktualisiert, die sich auf die Anschaffung von Anlagen bezieht. 

Sieht die aktuelle Systemkonfiguration vor, dass eine Anlagenanschaffung beim Buchen einer Rechnung gebucht wird, erfolgt die Buchung gemäß den im Modul "Anlagevermögen" festgelegten Buchungsprofilen für die unterschiedlichen Anlagenbuchungstypen. Die Buchung wird anhand der Anlage, des Wertmodells und der Anlagenbuchungsart gesteuert, die vor dem Buchen der Kreditorenrechnung auf der Seite **Bestellung** ausgewählt werden. 

Wenn das Wertmodell ein abgeleitetes Abschreibungsbuch umfasst, wird beim Buchen der Debitorenrechnung eine Kreditorenrechnung erstellt.

Die Integration wird auf der Registerkarte **Anlagen** lagen im Inforegister **Positionsdetails** auf der Seite **Bestellung** aktiviert. Sie können eine Bestellung für eine Anlage an den Kreditor senden. Allerdings werden die Anlagen und Hauptkonten nur aktualisiert, wenn Sie die Kreditorenrechnung nach dem Eingang der Anlage buchen. Da Bestellungen nur Lagerartikel enthalten können, hängt von den Einstellungen für die juristische Person ab, welche Auswirkungen die Anschaffung von Anlagen auf den Bestand hat.

## <a name="project-management-and-accounting"></a>Projektverwaltung und -verrechnung
Sie können ein Projekt einer Anlage zuordnen, die durch das Projekt betroffen ist. Zudem kann jede Phase, jede Aufgabe oder jedes Unterprojekt einer anderen Anlage zugeordnet werden. Jedem Projektdatensatz kann eine Anlage zugeordnet werden. Sie erstellen die Zuordnung, wenn Sie eine Anlagennummer im Nummernfeld **Anlagen** auf der Seite **Projekte** eingeben. Der Projekttyp muss entweder **Intern** oder **Kostenprojekt** sein. 

Sie können auch mithilfe der Seite**Projekte** Details zu Anlagen anzeigen, die Projekten zugeordnet sind. Klicken Sie zum Anzeigen des Anlagendatensatzes auf den Anlagenlink im Inforegister **Einstellungen**, um die Seite **Anlagen** zu öffnen. Klicken Sie anschließend auf **Projekt** &gt; **Alle Projekte**, um die Projekte anzuzeigen, die der Anlage zugeordnet sind. 

Eine Zuordnung von Anlagen zu Projekten wird üblicherweise dann vorgenommen, wenn die Projekte mit Arbeiten an der Anlage, mit der Wartung der Anlage oder mit Verbesserungen an der Anlage zusammenhängen. Nach Abschluss des Projekts erfolgt nicht automatisch eine Höherbewertung der Anlage. Diese muss ggf. manuell ausgeführt werden, wenn eine Höherbewertung erforderlich ist. 

Entfernen Sie auf der Seite **Anlagennummer** auf der Seite **Projekte** den Wert, um die Zuordnung zwischen einem Projekt und einer Anlage aufzuheben. 

Eine erstellte oder produzierte Anlage kann auch als Teil eines Vorkalkulationsprojekts ausgewiesen werden. Am Ende eines Vorkalkulationsprojekts kann dann automatisch eine Anlagenanschaffungsbuchung vorgenommen werden.

Weitere Informationen finden Sie unter[Anlagen über Beschaffung erhalten](acquire-assets-procurement.md).



