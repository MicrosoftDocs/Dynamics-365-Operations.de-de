---
title: Probleme mit dem Modul für duales Schreiben in Finance and Operations-Apps behandeln
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Modul Duales Schreiben in der Finance and Operations App zusammenhängen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172759"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Probleme mit dem Modul für duales Schreiben in Finance and Operations-Apps behandeln

[!include [banner](../../includes/banner.md)]



Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Common Data Service. Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Modul **Duales Schreiben** in der Finance and Operations App zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Sie können das Modul Duales Schreiben in der Finance and Operations App nicht laden

Wenn Sie die Seite **Duales Schreiben** nicht öffnen können durch Auswahl der Kachel **Duales Schreiben** im Arbeitsbereich **Datenmverwaltung**, ist der Datenintegrationsdienst wahrscheinlich ausgefallen. Erstellen Sie ein Support-Ticket, um einen Neustart des Datenintegrationsdienstes anzufordern.

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>Fehler beim Versuch, eine neue Entitätszuordnung zu erstellen

**Erforderliche Anmeldeinformationen zum Lösen des Problems:** Azure AD Mandant Admin

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, eine neue Entität für Duales Schreiben zu konfigurieren:

*Der Antwortstatuscode zeigt keinen Erfolg an: 401 (Nicht erlaubt)*

Dieser Fehler tritt auf, weil nur ein Azure AD Mandantenadministrator eine neue Entitätszuordnung hinzufügen kann.

Um das Problem zu beheben, melden Sie sich bei der Finance and Operations App als Azure AD Administratormandant an. Sie müssen auch ins Web.PowerApps.com gehen und Ihre Verbindung erneut bestätigen.

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Fehler beim Öffnen der Benutzeroberfläche Duales Schreiben

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, über den Arbeitsbereich **Datenmanagement** auf Duales Schreiben zuzugreifen:

*login.microsoftonline.com weigerte sich, eine Verbindung herzustellen.*

Um das Problem zu beheben, melden Sie sich über ein InPrivate-Fenster bei Microsoft Edge, ein Inkognito-Fenster in Chromium oder ein Inkognito-Fenster in Google Chrome an. Sie müssen auch Cookies von Drittanbietern entsperren oder löschen.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Fehler beim Verknüpfen der Umgebung für Duales Schreiben oder Hinzufügen einer neuen Entitätszuordnung

**Erforderliche Anmeldeinformationen zum Lösen des Problems:** Azure AD Mandant Admin

Beim Verknüpfen oder Erstellen von Zuordnungen kann der folgende Fehler auftreten:

*Antwortstatuscode zeigt keinen Erfolg an: 403 (Token-Austausch).<br> Sitzungs-ID: \<Ihre Sitzungs-ID\><br> Stammaktivitäts-ID: \<Ihre Stammaktivitäts-ID\>*

Dieser Fehler kann auftreten, wenn Sie nicht über ausreichende Berechtigungen verfügen, um Duales Schreiben zu verknüpfen oder Zuordnungen zu erstellen. Sie müssen ein Azure AD Mandantenadministratorkonto zum Verknüpfen von Umgebungen und Hinzufügen neuer Entitätszuordnungen verwenden. Nach dem Einrichten können Sie jedoch ein Nicht-Administratorkonto verwenden, um den Status zu überwachen und die Zuordnungen zu bearbeiten.

## <a name="error-when-you-stop-the-entity-mapping"></a>Fehler beim Beenden der Entitätszuordnung

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, die Entitätszuordnung zu aktivieren:

*\[verboten\], \[{„Status“: 403, „Quelle“:„“,„Nachricht“:„Fehler beim Token-Austausch: Benutzer darf nicht auf die Verbindung dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx“}\] zugreifen. Der Remote-Server hat einen Fehler zurückgegeben: (403) Verboten.*

Dieser Fehler tritt auf, wenn die verknüpfte Common Data Service Umgebung nicht verfügbar ist.

Erstellen Sie ein Ticket für das Datenintegrationsteam, um das Problem zu beheben. Fügen Sie die Netzwerkablaufverfolgung hinzu, damit das Datenintegrationsteam die Zuordnung als **wird nicht ausgeführt** im hinteren Ende markieren kann.
