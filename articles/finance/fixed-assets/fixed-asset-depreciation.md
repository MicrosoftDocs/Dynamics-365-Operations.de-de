---
title: Anlagenabschreibung
description: Dieser Artikel enthält eine Übersicht der Abschreibung in Anlagen.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4fedee481b4066c81671cf1fca3781c8c75aaeb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874522"
---
# <a name="fixed-asset-depreciation"></a>Anlagenabschreibung

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dieser Artikel enthält eine Übersicht der Abschreibung in Anlagen.

Eine Abschreibung ist eine periodische Buchung, die normalerweise den Wert des Anlagevermögens in der Bilanz verringert und in einem Gewinn- und Verlustkonto als Ausgabe gebucht wird. Folglich wird ein Hauptkonto normalerweise für die periodische Abschreibung in der Bilanz verwendet. Ein Gegenkonto ist ein Konto im Gewinn- und Verlustteil des Kontenplans.

Ab Version 10.0.24 ermöglicht die Anlagenbuchkonfigurationsoption **Positive Abschreibung berechnen** auf der Seite **Bücher** die Abschreibung, um eine erworbene Anlage mit negativem Buchwert (Haben) zu belasten.

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

Sie können freigegebene Kalender mithilfe der Seite **Steuerkalender** im Hauptbuch erstellen.

Weitere Informationen finden Sie untere [Abschreibungsmethoden und - konventionen](depreciation-methods-conventions.md). 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
