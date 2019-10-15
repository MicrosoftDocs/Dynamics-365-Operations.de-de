---
title: Umsatzerkennungsübersicht
description: Dieses Thema enthält Informationen zur Umsatzerkennungsfunktion. Diese Funktion stellt ein flexibles Framework bereit, mit dem Sie unternehmensspezifische Regeln zur Erfassung des Umsatzerlöspreises und des Umsatzerlöszeitplans für Aufträge mit mehreren Elementen definieren können.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: d1aeb0cf556582ff53ca00c6bb8d863a088950b9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184116"
---
# <a name="revenue-recognition-overview"></a>Umsatzerkennungsübersicht

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!NOTE]
> Die Umsatzerkennungsfunktion kann bisher nicht über die Funktionsverwaltung aktiviert werden. Sie müssen derzeit Konfigurationsschlüssel verwenden, um sie zu aktivieren.

Unternehmen in Branchen, bei denen Verkäufe auf mehreren Ebenen getätigt werden, wie beispielsweise Produkte, Services, Abonnements usw., müssen Aufträge mit mehreren Elementen erstellen können, sodass die Umsatzerlöse basierend auf unternehmensspezifischen wie branchenspezifischen Richtlinien erfasst werden können.

Im Allgemeinen lässt sich der Umsatzerkennungsprozess verwenden, um folgende Aufgaben auszuführen:

* Umsatzerlöse zuweisen – um sicherzustellen, dass der entsprechende Umsatzerlöspreis auf Grundlage der Komponentenwerte bei Aufträgen mit mehreren Elementen realisiert wird.
* Umsatzerlöse verzögern – basierend auf einem Umsatzerlöszeitplan, der den Vertragszeitrahmen und die prozentualen Anteile für Umsatzerlöse im Zeitverlauf erkennt, werden die Umsatzerlöse verzögert dargestellt.

Die Umsatzerkennungsfunktion stellt ein flexibles Framework bereit, mit dem Sie unternehmensspezifische Regeln zur Erfassung des Umsatzerlöspreises und des Umsatzerlöszeitplans definieren können.

Für die Umsatzerkennung werden Verkaufsauftragsdokumente für veröffentlichte Produkte verwendet. Die veröffentlichten Produkte enthalten die nötigen Informationen, um den Umsatzerlöspreis und den Umsatzerlöszeitplan festzulegen. Der Verkaufsauftrag kann aus einem Aufwandsprojekt stammen.

Unternehmen können die Umsatzerlöszeitplan-Funktionen ohne die Umsatzerlöspreis-Funktionen verwenden. Daher wird der Preis in den Verkaufsauftragspositionen entweder als Umsatzerlös oder als verzögerter Umsatzerlös verwendet. Wenn ein Umsatzerlöszeitplan für die Verkaufsauftragsposition vorhanden ist, wird der Preis für die Verkaufsauftragsposition verzögert. Wenn kein Umsatzerlöszeitplan für die Verkaufsauftragsposition vorhanden ist, wird der Preis für die Verkaufsauftragsposition auf einem Umsatzerlöskonto gebucht, wenn er in Rechnung gestellt wird.

Der Umsatzerlöspreis wird entweder berechnet, wenn der Verkaufsauftrag bestätigt wurde oder wenn die Rechnung gebucht wird. Um eine Vorschau des Umsatzerlöspreises anzuzeigen, bevor die Rechnung gebucht wird, müssen Sie den Verkaufsauftrag bestätigen.

Nach der Bestätigung des Verkaufsauftrags wird auch ein Zeitplan für den voraussichtlichen Umsatzerlös erstellt, falls eine Verkaufsauftragsposition einen Umsatzerlöszeitplan enthält. Wenn der Verkaufsauftrag in Rechnung gestellt wird, wird der Zeitplan für den voraussichtlichen Umsatzerlös gelöscht, und der Zeitplan für den voraussichtlichen Umsatzerlös wird durch den tatsächlichen Umsatzerlöszeitplan ersetzt.

Die Details des Umsatzerkennungszeitplans werden für jede Auftragsposition verwaltet. Daher kann der Umsatzerkennungsmanager die Details anzeigen und Positionen für den Umsatzerlös freigeben, wenn die vertragliche Verpflichtung abgeschlossen wurde. Am Ende jeder Periode kann der Umsatzerkennungsmanager eine Umsatzerlöserfassung erstellen, um alle Zeitplanpositionen freizugeben, die an oder vor einem definierten Datum fällig werden. Diese Umsatzerlöserfassung wird nicht sofort gebucht. Daher kann der Umsatzerkennungsmanager überprüfen, ob die richtigen Beträge aus dem verzögerten Umsatzerlös aus dem tatsächlichen Umsatz freigegeben werden.

Wenn eine Vertragsänderung dafür sorgt, dass eine neue Verkaufsauftragsposition entweder dem vorhandenen Verkaufsauftrag oder einem neuen Verkaufsauftrag hinzugefügt wird, kann ein Umlegungsverfahren ausgeführt werden, um den Umsatzerlöspreis für alle Positionen in allen Verkaufsaufträgen zu berichtigen.
