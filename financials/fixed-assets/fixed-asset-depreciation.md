---
title: Anlagenabschreibung
description: "Dieser Artikel enthält eine Übersicht der Abschreibung von Anlagen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a7f27847832e7c4814f1dc5982b6352c2ba98741
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="fixed-asset-depreciation"></a>Anlagenabschreibung

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält eine Übersicht der Abschreibung von Anlagen.

Eine Abschreibung ist eine periodische Buchung, die normalerweise den Wert des Anlagevermögens in der Bilanz verringert und in einem Gewinn- und Verlustkonto als Ausgabe gebucht wird. Folglich wird ein Hauptkonto normalerweise für die periodische Abschreibung in der Bilanz verwendet. Ein Gegenkonto ist ein Konto im Gewinn- und Verlustteil des Kontenplans.

## <a name="depreciation-adjustment"></a>Abschreibungsregulierung
Normalerweise wird nur eine Korrektur an einer bereits gebuchten Abschreibungsbuchung als Abschreibungsanpassung gebucht. Daher werden das Hauptkonto und das Gegenkonto ebenso wie die Konten für die Abschreibung eingerichtet. Bei einer Abschreibungsanpassung kann es sich um einen positiven oder einen negativen Betrag handeln, jedoch bleiben das Hauptkonto (als Bilanzkonto) und das Gegenkonto (normalerweise als Gewinn- und Verlustkonto) funktionell gleich.

## <a name="extraordinary-depreciation"></a>Außerordentliche Abschreibung
Außerordentliche Abschreibungen funktionieren wie normale Abschreibungen. Folglich wird ein Hauptkonto verwendet, um den Abschreibungsbetrag in der Bilanz zu buchen und den Wert der Anlage zu verringern. Ein Gegenkonto ist ein GuV-Konto, in dem die Abschreibung, die für das Geschäftsjahr berechnet wird, als Ausgabe berechnet wird. 

Eine außerordentliche Abschreibung ist von der grundlegenden Abschreibung unabhängig. Wurde die außerordentliche Abschreibung als separate Buchungsart eingerichtet, kann die außerordentliche Abschreibung getrennt von der normalen grundlegenden Abschreibung gebucht und gemeldet werden.

## <a name="special-depreciation-allowance"></a>Sonderabschreibung
Die Sonderabschreibung ermöglicht Ihnen, im ersten Jahr der Inbetriebnahme und Abschreibung einer Anlage zusätzliche Abschreibungsbeträge geltend zu machen. Die Sonderabschreibung muss vor jeder anderen Abschreibungsberechnung durchgeführt werden. Da Sonderabschreibungen bis vor kurzem für die Nutzungsdauer der Anlage unbekannt waren, empfiehlt es sich, diese Art Abschreibungsbetrag mit einem Buch zu verwenden, mit dem nicht im Hauptbuch gebucht wird. Mithilfe der Funktion "Buchungen löschen, die nicht im Hauptbuch gebucht werden" können Sie historische Transaktionen für diese Bücher löschen. Sie können die Abschreibungshistorie zum Anlagenbuch dann löschen, buchen die Sonderabschreibung, wenn dieses bekannt hat, und die restlichen Abschreibungsbuchungen für das Jahr dann buchen. 

Sie können eine unbegrenzte Anzahl von Datensätzen für die Sonderabschreibung erstellen. Nach deren Zuordnung zu einem Anlagengruppenbuch werden sie auf das Anlagenbuch angewendet. 

Die Sonderabschreibung wird entweder als Prozentsatz oder als fester Wert eingegeben. Beim Buchen von Abschreibungsvorschlägen werden Buchungen für Sonderabschreibungen im Abschreibungsbuch getrennt von Abschreibungsbuchungen erfasst.

## <a name="depreciation-calendars"></a>Abschreibungskalender
Jedes Abschreibungsbuch hat einen Kalender, der verwendet wird, wenn Sie Anlagen abschreiben. Das Buch verwendet standardmäßig den Sachkontosteuerkalender, wenn Sie keinen Kalender angeben. Sie müssen einen Steuerkalender für ein Buch auswählen, wenn das entsprechende Abschreibungsprofil des Buchs ein steuerlich relevantes Abschreibungsjahr verwendet. 

Sie können freigegebene Kalender mithilfe der Seite **Steuerkalender**im Hauptbuch erstellen.

Weitere Informationen finden Sie untere [Abschreibungsmethoden und - konventionen](depreciation-methods-conventions.md). 




