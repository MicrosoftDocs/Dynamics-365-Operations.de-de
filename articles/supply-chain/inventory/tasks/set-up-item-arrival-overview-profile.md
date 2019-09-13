---
title: Übersichtsprofil zum Wareneingang einrichten
description: In diesem Thema geht es um die Einrichtung eines Ankunftsübersichtsprofils.
author: ShylaThompson
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1c6bcbb71f52e0ec5f979f8d79c896d10689a1b
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867226"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>Übersichtsprofil zum Wareneingang einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Thema geht es um die Einrichtung eines Ankunftsübersichtsprofils. Das Wareneingangsübersichtprofil ist eine Regelsammlung, die angewendet werden, wenn die Wareneingangsübersichtseite von einem Benutzer geöffnet wird. Sie können diese Prozedur im Demodatunternehmen USMF verwenden. Diese Prozedur wird normalerweise von einem Sachbearbeiter Zugänge ausgeführt.

1. Gehen Sie im Navigationsbereich zu **Module > Bestandsverwaltung > Einrichtung > Verteilung > Verteilung > Ankunftsübersichtsprofile**.
2. Wählen Sie **Neu** aus. Da Sie fast immer im gleichen Lagerort zusammenarbeiten, der vollständige LKW-Auslastungen auslädt, sollten Sie ein Wareneingangsübersichtprofil erstellen, um den Vorgang des zum Erfassen der empfangenen Artikeln zu vereinfachen.  
3. Geben Sie im Feld **Ankunftsübersicht Profilname** einen Wert ein.
4. Wählen Sie im Feld **Zeilen anzeigen** eine Option aus. Wählen Sie aus, welche Zeilen für die Belege angezeigt werden sollen:  

    - **Alle** - Zeigt alle Zeilen an, unabhängig vom Status.   
    - **In Bearbeitung** - Zeigt Zeilen für Belege an, in denen der Fortschritt vollständig oder teilweise ist. Dies bedeutet, dass die Menge für jede Position vollständig oder teilweise in einer Wareneingangserfassung erfasst wurde.   
    - **Nicht vollständig** - Zeigt Zeilen für Belege an, bei denen der Fortschritt None oder Partly ist. Dies bedeutet, dass für jede Position keine oder nur ein Teil der Menge in einer Wareneingangserfassung erfasst wurde.  

5. Erweitern oder komprimieren Sie den Abschnitt **Anreiseoptionen**.
6. Geben Sie im Feld **Tage vorwärts** einen Wert ein. Damit werden die einen Filter festgelegt, um die Zugangspositionen anzeigen, die erwartet werden, innerhalb der nächsten Tage Zustellung des (abhängig von der Anzahl Sie festgelegt wurde).  
7. Geben Sie im Feld **Tage zurück** einen Wert ein. Damit werden die einen Filter festgelegt, um die Zugangspositionen anzeigen, die erwartet werden, mehrere Tage aktuellen Monat empfangen zu werden.  
8. Geben Sie in das Feld **Lager** einen Wert ein. Filtern Sie nach einen oder mehrere Lagerorte.  
9. Wählen Sie im Feld **Lieferart** einen Wert aus. Damit wird einen Filter festgelegt, um nur die Zugangspositionen mit diesem Lieferart anzuzeigen.  
10. Wählen Sie im Feld **Name** WHS.
11. Wählen Sie im Feld **Lager** Lager 24. Dies ist der Standardlagerort, der für registrierte Zugangspositionen verwendet wird, die dieses Profil verwenden.  
12. Wählen Sie im Feld **Standort** **Baydoor**. Dies ist der Standardlagerort, der für registrierte Zugangspositionen verwendet wird, die dieses Profil verwenden.  
13. Erweitern oder komprimieren Sie den Abschnitt **Ankunftsabfrage Details**.
14. Wählen Sie im Feld **Einschränken auf Standort** den Standort 2 aus. Damit wird einen Filter festgelegt, um nur die Zugangspositionen an diesem Lagerort anzuzeigen.  
15. Setzen Sie die Option **Bestellungen** auf **Ja**. Wählen Sie Positionen aus offenen Bestellungen aus.  
16. Stellen Sie die Option **Transfer** Bestellungen auf **Ja**. Wählen Sie Positionen aus offenen Umlagerungsaufträgen aus.  
17. Wählen Sie **Speichern**.
18. Schließen Sie die Seite.

