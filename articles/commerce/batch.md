---
title: Verbesserte Handhabung von Artikeln mit Chargenverfolgung
description: Dieses Thema behandelt die vorgenommenen Verbesserungen bei der Handhabung von Artikeln mit Chargenverfolgung beim Aufstellungsbuchungsprozess.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: ef946df30c68373b83660fce98b472dc94b42719
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989592"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Verbesserte Handhabung von Artikeln mit Chargenverfolgung


[!include [banner](includes/banner.md)]


In der Verkaufsstelle (POS) können für Artikel mit Chargenverfolgung zum Zeitpunkt des Verkaufs keine POS-Chargennummern erfasst werden. Bei bestimmten Konfigurationen aber, wenn Umsätze am Hauptsitz mittels Kundenaufträgen oder Auszugsbuchungen gebucht werden, wird im Microsoft Dynamics-System davon ausgegangen, dass für Artikel mit Chargenverfolgung gültige Chargennummern vorliegen und bei der Rechnungsabwicklung verwendet werden.

Wenn gültige Chargennummern für Produkte vorhanden sind, werden sie vom Prozess zur Berechnung von Debitorenaufträgen und Aufträgen der Auszugsbuchung verwendet. Andernfalls kann die Debitorenrechnung nicht gebucht werden und der POS-Benutzer erhält eine Fehlermeldung. Die Auszugsbuchung wechselt dann in den Fehlerstatus. Dieser Fehlerstatus tritt auf, wenn für die Produkte ein negativer Bestand aktiviert wird.

Dank der Verbesserungen, die in Retail ab Version 10.0.4 vorgenommen wurden, wird bei Artikeln, deren Bestand 0 (null) ist oder wenn keine Chargennummer vorhanden ist, die Berechnung von Debitorenaufträgen und Aufträgen durch die Auszugsbuchung nicht blockiert, wenn für Artikel mit Chargenverfolgung ein negativer Bestand aktiviert wird. Sind keine Chargennummern vorhanden, verwendet die neue Funktion für die Verkaufspositionen eine Standardkennung.

Um die Standardchargenkennung für Debitorenaufträge festzulegen, legen Sie auf der Seite **Handelsparameter** auf der Registerkarte **Debitorenaufträge** auf dem Inforegister **Auftrag** das Feld **Standardchargenkennung** fest.

Um die Standardchargenkennung für die Berechnung von Aufträgen im Zuge der Auszugsbuchung festzulegen, legen Sie auf der Seite **Handelsparameter** auf der Registerkarte **Buchung** auf dem Inforegister **Lageraktualisierung** das Feld **Standardchargenkennung** fest.

> [!NOTE]
> Diese Funktion ist nur dann verfügbar, wenn für den entsprechenden Filiallagerort und die Artikel die erweiterte Lagerung aktiviert ist. In einer späteren Version wird die Funktion auch in Fällen unterstützt, in denen keine erweiterte Lagerung verwendet wird.

> [!NOTE]
> Die Unterstützung für eine verbesserte Handhabung von per Stapel nachverfolgten Artikeln bei der Aufstellungsbuchung einfacher Lagerverwaltungsszenarien wurde in Retail-Version 10.0.5 eingeführt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]