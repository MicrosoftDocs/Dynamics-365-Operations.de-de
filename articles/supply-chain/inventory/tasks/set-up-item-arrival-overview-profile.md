---
title: "Übersichtsprofil zum Wareneingang einrichten"
description: "Dieser Aufgabe konzentriert sich auf den Einstellungen eines Wareneingangsübersichtprofils."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: b971e72febbd78ff7c27ad2029e5061b978dc44e
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-an-item-arrival-overview-profile"></a>Übersichtsprofil zum Wareneingang einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Dieser Aufgabe konzentriert sich auf den Einstellungen eines Wareneingangsübersichtprofils. Das Wareneingangsübersichtprofil ist eine Regelsammlung, die angewendet werden, wenn die Wareneingangsübersichtseite von einem Benutzer geöffnet wird. Sie können diese Prozedur im Demodatunternehmen USMF verwenden. Diese Prozedur wird normalerweise von einem Sachbearbeiter Zugänge ausgeführt.





1. Wechseln Sie zu Lagerverwaltung > Einrichtung > Verteilung > Wareneingangsübersichtprofile.
2. Klicken Sie auf "Neu".
    * Da Sie fast immer im gleichen Lagerort zusammenarbeiten, der vollständige LKW-Auslastungen auslädt, sollten Sie ein Wareneingangsübersichtprofil erstellen, um den Vorgang des zum Erfassen der empfangenen Artikeln zu vereinfachen.  
3. Geben Sie im Feld Ankunftsübersichts-Profilname einen Wert ein.
4. Wählen Sie im Feld 'Zeilen anzeigen' eine Option aus.
    * Wählen Sie aus, welche Positionen für die Zugänge angezeigt werden sollen: Alle - Alle Positionen anzeigenm, unabhängig vom Status.   In Bearbeitung – Zeigen Sie Positionen für Zugänge an, deren Bearbeitung den Status Komplett oder Teilweise aufweist. Dies bedeutet, dass die Menge für jede Position vollständig oder teilweise in einer Wareneingangserfassung erfasst wurde.   Nicht vollständig – Zeigen Sie Positionen für Zugänge an, deren Bearbeitung den Status Keiner oder Teilweise aufweist. Dies bedeutet, dass für jede Position keine oder nur ein Teil der Menge in einer Wareneingangserfassung erfasst wurde.  
5. Erweitern oder reduzieren Sie den Abschnitt "Wareneingangsoptionen".
6. Geben Sie im Feld Tage im Voraus einen Wert ein.
    * Damit werden die einen Filter festgelegt, um die Zugangspositionen anzeigen, die erwartet werden, innerhalb der nächsten Tage Zustellung des (abhängig von der Anzahl Sie festgelegt wurde).  
7. Geben Sie im Feld Tage zurück einen Wert ein.
    * Damit werden die einen Filter festgelegt, um die Zugangspositionen anzeigen, die erwartet werden, mehrere Tage aktuellen Monat empfangen zu werden.  
8. Geben Sie im Feld Lagerorte einen Wert ein.
    * Filtern Sie nach einen oder mehrere Lagerorte.  
9. Wählen Sie im Feld "Lieferart" einen Wert aus.
    * Damit wird einen Filter festgelegt, um nur die Zugangspositionen mit diesem Lieferart anzuzeigen.  
10. Wählen Sie im Feld "Name" die Option "WHS" aus.
11. Wählen Sie im Feld "Lagerort" den Lagerort 24 aus.
    * Dies ist der Standardlagerort, der für registrierte Zugangspositionen verwendet wird, die dieses Profil verwenden.  
12. Wählen Sie im Feld "Lagerplatz" die Option "Ladebereichstor" aus.
    * Dies ist der Standardlagerort, der für registrierte Zugangspositionen verwendet wird, die dieses Profil verwenden.  
13. Erweitern oder reduzieren Sie den Abschnitt "Wareneingangs-Abfragedetails".
14. Wählen Sie im Feld "Auf Standort beschränken" den Standort 2 aus.
    * Damit wird einen Filter festgelegt, um nur die Zugangspositionen an diesem Lagerort anzuzeigen.  
15. Legen Sie die Option "Bestellungen" auf "Ja" fest.
    * Wählen Sie Positionen aus offenen Bestellungen aus.  
16. Legen Sie die Option "Umlagerungsaufträge" auf "Ja" fest.
    * Wählen Sie Positionen aus offenen Umlagerungsaufträgen aus.  
17. Klicken Sie auf "Speichern".
18. Schließen Sie die Seite.

