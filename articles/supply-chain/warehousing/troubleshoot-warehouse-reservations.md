---
title: Fehlerbehebung bei Reservierungen in der Lagerortverwaltung
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Lagerort-Reservierungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a9a5d20732a802fc58c392853af8334bbc07de73
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248714"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Fehlerbehebung bei Reservierungen in der Lagerortverwaltung

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Lagerort-Reservierungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>Ich erhalte die folgende Fehlermeldung: „Reservierungen können nicht entfernt werden, da Arbeit erstellt wurde, die sich auf die Reservierungen stützt.“

### <a name="issue-description"></a>Problembeschreibung

Sie können die Reservierung von Bestand in einer Zeile nicht aufheben, weil es offene Arbeit gegen die Zeile gibt.

### <a name="issue-resolution"></a>Problemlösung

Untersuchen Sie, ob offene Packgruppenarbeit existiert, um das Element von einem Packplatz zu einem anderen Lagerplatz zu bringen (z. B. *Baydoor*). Überprüfen Sie die Datensätze auf den Seiten **Arbeitserstellungsprotokoll** und **Arbeitsdetails**, um festzustellen, was den Bestand physisch reserviert, und schließen Sie dann die Arbeit ab oder löschen Sie sie, um die Reservierung freizugeben.

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>Ich erhalte die folgende Fehlermeldung: „Bestandsmenge - %1 konnte nicht aktualisiert werden, da nicht genügend Bestandstransaktionen für Element %2.... vorliegen.“

### <a name="issue-description"></a>Problembeschreibung

Dieses Problem kann auftreten, wenn das System eine Bestandsmenge nicht aktualisieren kann, weil es nicht genügend Bestandstransaktionen gibt, die die angegebenen Dimensionen haben. Hier ist der vollständige Text der Fehlermeldung:

> Bestandsmenge -%1 konnte nicht aktualisiert werden, da nicht genügend Bestandstransaktionen für Element %2 mit den Dimensionen Größe=%3, Farbe=%4, Zugänge=%5, Standort=%6, Lagerort=%7, Ort=%8, Bestandsstatus=Verfügbar, Ladungsträger=%9, Chargennummer=%10 für Referenz-ID %11 auf Los-ID %12.

### <a name="issue-resolution"></a>Problemlösung

Stellen Sie sicher, dass keine Bestandstransaktionen die Menge physisch reservieren. Diese Transaktionen könnten z. B. Qualitätsaufträge, Bestandssperrsätze oder Ausgabeaufträge öffnen.

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>Ich erhalte die folgende Fehlermeldung: „Physischer Bestand...kann nicht reserviert werden, da nur 0,00 im Bestand vorhanden sind.“

### <a name="issue-description"></a>Problembeschreibung

Dieses Problem kann auftreten, wenn das System eine Bestandsmenge nicht aktualisieren kann, weil es nicht genügend Bestandstransaktionen gibt, die die angegebenen Dimensionen haben. Hier ist der vollständige Text der Fehlermeldung:

> Physischer Bestand Standort=%1, Lagerort=%2, Bestandsstatus=Verfügbar, Chargennummer=%3, Besitzer=%4: %5 kann nicht reserviert werden, da nur 0,00 im Bestand verfügbar sind.

### <a name="issue-resolution"></a>Problemlösung

Dieses Problem wird wahrscheinlich durch offene Arbeit verursacht. Beenden Sie entweder die Arbeit oder empfangen Sie ohne Arbeitserstellung. Stellen Sie sicher, dass keine Bestandstransaktionen die Menge physisch reservieren. Diese Vorgänge können z. B. offene Qualitätsaufträge, Bestandssperrungen oder Ausgabeaufträge sein.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Ich erhalte die folgende Fehlermeldung: „Um einer Welle zugewiesen zu werden, müssen Ladungszeilen die Dimensionen oberhalb des Lagerplatzes angeben. Um diese Dimensionen zuzuweisen, reservieren Sie und erstellen Sie die Ladelinie neu.“

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie ein Element verwenden, das eine Reservierungshierarchie „Charge oben“ hat (mit der Dimension **Chargennummer**, die *über* der Dimension **Lagerplatz** platziert ist), funktioniert der Befehl **Freigeben an Lagerort** auf der Seite **Ladungsplanung Workbench** für eine Teilmenge nicht. Sie erhalten diese Fehlermeldung, und es wird keine Arbeit für die Teilmenge erstellt.

Wenn Sie jedoch ein Element verwenden, das eine Reservierungshierarchie „Charge unten“ hat (mit der Dimension **Chargennummer**, die *unter* der Dimension **Lagerplatz** platziert ist), können Sie auf der Seite **Ladungsplanung Werkbank** für eine Teilmenge eine Ladung freigeben.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten ist beabsichtigt. Wenn Sie in der Reservierungshierarchie eine Dimension oberhalb der **Ort**-Dimension einlagern, muss diese vor der Freigabe zum Lagerort angegeben werden. Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion bei Freigaben an das Lagerort aus der Ladeplanungs-Workbench handelt. Teilmengen können nicht freigegeben werden, wenn eine oder mehrere Dimensionen über **Lagerplatz** nicht angegeben sind.

Weitere Informationen finden Sie unter [Flexible Richtlinie für die Reservierung von Dimensionen auf Lagerebene](flexible-warehouse-level-dimension-reservation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]