---
title: Übersicht zur Umsatzerkennung
description: Dieses Thema enthält Informationen zur Umsatzerkennungsfunktion. Diese Funktion stellt ein flexibles Framework bereit, mit dem Sie unternehmensspezifische Regeln zur Erfassung des Umsatzerlöspreises und des Umsatzerlöszeitplans bei Aufträgen mit mehreren Elementen festlegen können.
author: kweekley
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: edc0bab7287e271f1d1197d87a95709599e12b5b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820544"
---
# <a name="revenue-recognition-overview"></a>Übersicht zur Umsatzerkennung

[!include [banner](../includes/banner.md)]

Unternehmen in Branchen, bei denen Verkäufe auf mehreren Ebenen getätigt werden, wie beispielsweise Produkte, Services, Abonnements usw., müssen Aufträge mit mehreren Elementen erstellen können, damit Umsatzerlöse basierend auf unternehmens- sowie branchenspezifischen Richtlinien erfasst werden können.

> [!NOTE]
> Die Funktion zur Umsatzerkennung kann nicht mithilfe der Funktionsverwaltung aktiviert werden. Derzeit erfolgt die Aktivierung mit Konfigurationsschlüsseln.

> Die Umsatzerkennung, einschließlich Bündelfunktion, wird in Commerce-Kanälen (E-Commerce, POS, Callcenter) nicht unterstützt. Mit Umsatzerkennung konfigurierte Artikel dürfen nicht in Bestellungen oder Transaktionen ergänzt werden, die in Commerce-Kanälen erstellt wurden.

Im Allgemeinen dient die Umsatzerkennung zur Erledigung folgender Aufgaben:

* Umsatzerlöse zuweisen – um sicherzustellen, dass der entsprechende Umsatzerlöspreis bei Aufträgen mit mehreren Elementen auf den Werten der Bestandteile beruht.
* Umsatzerlöse verzögern – basierend auf einem Umsatzerlöszeitplan, der den Vertragszeitrahmen und die prozentualen Anteile für Umsatzerlöse im Zeitverlauf erkennt, werden die Umsatzerlöse verzögert dargestellt.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

Das Video [Verwendung der Umsatzerkennung in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (oben) ist in der [Finance and Operations-Playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) auf YouTube enthalten.

Die Umsatzerkennungsfunktion stellt ein flexibles Framework bereit, mit dem Sie unternehmensspezifische Regeln zur Erfassung des Umsatzerlöspreises und des Umsatzerlöszeitplans definieren können.

Für die Umsatzerkennung werden Verkaufsauftragsdokumente für veröffentlichte Produkte verwendet. Die veröffentlichten Produkte enthalten die nötigen Informationen, um den Umsatzerlöspreis und den Umsatzerlöszeitplan festzulegen. Der Verkaufsauftrag kann aus einem Aufwandsprojekt stammen.

Unternehmen können die Umsatzerlöszeitplan-Funktionen ohne die Umsatzerlöspreis-Funktionen verwenden. Daher wird der Preis in den Verkaufsauftragspositionen entweder als Umsatzerlös oder als verzögerter Umsatzerlös verwendet. Wenn ein Umsatzerlöszeitplan für die Verkaufsauftragsposition vorhanden ist, wird der Preis für die Verkaufsauftragsposition verzögert. Wenn kein Umsatzerlöszeitplan für die Verkaufsauftragsposition vorhanden ist, wird der Preis für die Verkaufsauftragsposition auf einem Umsatzerlöskonto gebucht, wenn er in Rechnung gestellt wird.

Der Umsatzerlöspreis wird entweder berechnet, wenn der Verkaufsauftrag bestätigt wurde oder wenn die Rechnung gebucht wird. Um eine Vorschau des Umsatzerlöspreises anzuzeigen, bevor die Rechnung gebucht wird, müssen Sie den Verkaufsauftrag bestätigen.

Nach der Bestätigung des Verkaufsauftrags wird auch ein Zeitplan für den voraussichtlichen Umsatzerlös erstellt, falls eine Verkaufsauftragsposition einen Umsatzerlöszeitplan enthält. Wenn der Verkaufsauftrag in Rechnung gestellt wird, wird der Zeitplan für den voraussichtlichen Umsatzerlös gelöscht, und der Zeitplan für den voraussichtlichen Umsatzerlös wird durch den tatsächlichen Umsatzerlöszeitplan ersetzt.

Die Details des Umsatzerkennungszeitplans werden für jede Auftragsposition verwaltet. Daher kann der Umsatzerkennungsmanager die Details anzeigen und Positionen für den Umsatzerlös freigeben, wenn die vertragliche Verpflichtung abgeschlossen wurde. Am Ende jeder Periode kann der Umsatzerkennungsmanager eine Umsatzerlöserfassung erstellen, um alle Zeitplanpositionen freizugeben, die an oder vor einem definierten Datum fällig werden. Diese Umsatzerlöserfassung wird nicht sofort gebucht. Daher kann der Umsatzerkennungsmanager überprüfen, ob die richtigen Beträge aus dem verzögerten Umsatzerlös aus dem tatsächlichen Umsatz freigegeben werden.

Wenn eine Vertragsänderung dafür sorgt, dass eine neue Verkaufsauftragsposition entweder dem vorhandenen Verkaufsauftrag oder einem neuen Verkaufsauftrag hinzugefügt wird, kann ein Umlegungsverfahren ausgeführt werden, um den Umsatzerlöspreis für alle Positionen in allen Verkaufsaufträgen zu berichtigen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]