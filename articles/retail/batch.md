---
title: Verbesserte Handhabung von Artikeln mit Chargenverfolgung
description: Dieses Thema behandelt die vorgenommenen Verbesserungen bei der Handhabung von Artikeln mit Chargenverfolgung beim Buchen des Einzelhandelsauszugs.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 5bbddf649f66ded9588cdb1e3f43c75630dc248a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770162"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Verbesserte Handhabung von Artikeln mit Chargenverfolgung


[!include [banner](includes/banner.md)]


In Retail Point of Sale (POS) können für Artikel mit Chargenverfolgung zum Zeitpunkt des Verkauf keine Chargennummern erfasst werden. Bei bestimmten Konfigurationen aber, wenn Umsätze am Hauptsitz mittels Kundenaufträgen oder Auszugsbuchungen gebucht werden, wird im Microsoft Dynamics-System davon ausgegangen, dass für Artikel mit Chargenverfolgung gültige Chargennummern vorliegen und bei der Rechnungsabwicklung verwendet werden.

Wenn gültige Chargennummern für Produkte vorhanden sind, werden sie vom Prozess zur Berechnung von Debitorenaufträgen und Aufträgen der Auszugsbuchung verwendet. Andernfalls kann die Debitorenrechnung nicht gebucht werden und der POS-Benutzer erhält eine Fehlermeldung. Die Auszugsbuchung wechselt dann in den Fehlerstatus. Dieser Fehlerstatus tritt auf, wenn für die Produkte ein negativer Bestand aktiviert wird.

Dank der Verbesserungen, die in Retail ab Version 10.0.4 vorgenommen wurden, wird bei Artikeln, deren Bestand 0 (null) ist oder wenn keine Chargennummer vorhanden ist, die Berechnung von Debitorenaufträgen und Aufträgen durch die Auszugsbuchung nicht blockiert, wenn für Artikel mit Chargenverfolgung ein negativer Bestand aktiviert wird. Sind keine Chargennummern vorhanden, verwendet die neue Funktion für die Verkaufspositionen eine Standardkennung.

Um die Standardchargenkennung für Debitorenaufträge festzulegen, legen Sie auf der Seite **Einzelhandelsparameter** auf der Registerkarte **Debitorenaufträge** auf dem Inforegister **Auftrag** das Feld **Standardchargenkennung** fest.

Um die Standardchargenkennung für die Berechnung von Aufträgen im Zuge der Auszugsbuchung festzulegen, legen Sie auf der Seite **Einzelhandelsparameter** auf der Registerkarte **Buchung** auf dem Inforegister **Lageraktualisierung** das Feld **Standardchargenkennung** fest.

> [!NOTE]
> Diese Funktion ist nur dann verfügbar, wenn für den entsprechenden Filiallagerort und die Artikel die erweiterte Lagerung aktiviert ist. In einer späteren Version wird die Funktion auch in Fällen unterstützt, in denen keine erweiterte Lagerung verwendet wird.

> [!NOTE]
> Die Unterstützung für eine verbesserte Handhabung von per Stapel nachverfolgten Artikeln bei der Aufstellungsbuchung einfacher Lagerverwaltungsszenarien wurde in Retail-Version 10.0.5 eingeführt.
