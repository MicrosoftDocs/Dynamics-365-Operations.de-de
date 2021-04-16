---
title: Fehlerbehebung bei Reservierungen in der Lagerortverwaltung
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Lagerort-Reservierungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828105"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Fehlerbehebung bei Reservierungen in der Lagerortverwaltung

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Lagerort-Reservierungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.

Informationen zu Themen, die sich auf die Registrierung von Chargen- und Seriennummern beziehen, finden Sie unter [Problembehandlung bei Chargen- und Serienreservierungshierarchien für Lagerorte](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
