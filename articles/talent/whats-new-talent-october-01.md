---
title: Neuerungen oder Änderungen in Dynamics 365 Talent – Core HR (1. Oktober 2018)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent – Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ba7c84e5b1d15fb7a4894af31bbf6793b402b9e4
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008753"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-1-2018"></a>Neuerungen oder Änderungen in Dynamics 365 Talent: Core HR (1. Oktober 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.1035.0**

In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.

## <a name="turn-off-electronic-payment-validation"></a>Prüfung elektronischer Zahlungen deaktivieren

Die Informationensprüfung der elektronischen Zahlung erfolgt, wenn Sie direkte Auszahlungen für die Einzahlung entweder durch **Mitarbeiter-Self-Service** (ESS )oder direkt im Formular Mitarbeiter verwenden. Diese Option ermöglicht die Flexibilität, diese Prüfung zu entfernen, wenn Sie die Prüfungsschecks nicht für Beträge und Restwerte benötigen. Diese Funktion ist hilfreich, wenn Sie von einem externen Lohnbuchhaltungssystem integrieren, das andere Anforderungen hat.

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a>Manager-Self-Service - Fügen Sie Ziele für Teammitglieder durch die Teamleistungszielkachel hinzu

Vor dieser Version können Manager Ziele ihrer Mitarbeiter individuell über die Leistungszielen hinzufügen, die den einzelnen Mitarbeitern zugeordnet werden. Mit dieser Aktualisierung können Manager auf die Kachel **Teamleistungsziele** zugreifen und neue Ziele erstellen, indem Sie beliebige direkte Mitarbeiter der Manager auswählen.

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a>Manager-Self-Service - Fügen Sie Üperprüfungen für Teammitglieder durch die Teamleistungsüberprüfungskachel hinzu

Vor dieser Version können Manager Überprüfungen ihrer Mitarbeiter individuell über die Leistungsüberprüfungen hinzufügen, die den einzelnen Mitarbeitern zugeordnet werden. Mit dieser Aktualisierung können Manager auf die Kachel **Teamleistungsüberprüfungen** zugreifen und neue Überprüfungen zu erstellen, indem Sie beliebige direkte Mitarbeiter der Manager auswählen.

## <a name="configure-proration-options-by-leave-plan"></a>Konfigurieren Sie Verrechnungsoptionen nach Urlaubplan

Organisationsprämienfreizeit unterschiedlich auf der Basis, wenn Mitarbeiter das Unternehmen wechseln‌ das Unternehmen eintreten. Bei einigen Organisationen wird den Mitarbeitern die vollständige Zuteilung an ihrem Startdatum bewilligt, während andere die Prämie aufteilen. Neue Optionen werden in dieser Version bereitgestellt, und zwar kann ausgewählt werden, wie die Prämien und die Abgrenzung für neue und ausscheidende Mitarbeiter in der Organisation erfolgt. Optionen enthalten: Aufgeteilt, vollständige Abgrenzung und keine Abgrenzung.

## <a name="other-changes"></a>Andere Änderungen

-   Mitarbeiterentität aktualisiert - Der Toteö **Persönlich** kann nun unter Verwendung des Excel-Add-Ins/Datenverwaltung aktualisiert werden.

-   Sicherheitsänderung, um das Entfernen der Schaltflächen **Löschen** und **Deaktivieren** im Mitarbeiter- Self-Service für Zahlungsinformationen zuzulassen.

## <a name="known-issue"></a>Bekannte Probleme

-   **Problem:** Wenn einer Arbeitskraft ein neuer Anhang hinzugefügt wird, werden die Schaltflächen **Neu** und **Bearbeiten** abgeblendet. **Problemumgehung:**, Bevor die Anhangsseite geöffnet wird, überprüfen Sie, dass die Infoboxen **Arbeitskraft** geschlossen werden. Wenn die Infoboxen geschlossen werden, wenn die **Arbeitskraft**-Seite geladen wird, werden die **Anhang**schaltflächen aktiviert. (Dieses Problem wird in der folgenden Plattformaktualisierung korrigiert.)
