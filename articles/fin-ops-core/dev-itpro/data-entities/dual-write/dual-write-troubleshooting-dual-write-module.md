---
title: Probleme mit dem dualen Scheiben in Finance and Operations-Apps behandeln
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 3ffeb2de0acc1761bccf62a1a124852c504e2a3a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131244"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Probleme mit dem dualen Scheiben in Finance and Operations-Apps behandeln

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse. Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Modul **Duales Schreiben** in der Finance and Operations App zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Sie können das Modul Duales Schreiben in der Finance and Operations App nicht laden

Wenn Sie die Seite **Duales Schreiben** nicht öffnen können durch Auswahl der Kachel **Duales Schreiben** im Arbeitsbereich **Datenmverwaltung**, ist der Datenintegrationsdienst wahrscheinlich ausgefallen. Erstellen Sie ein Support-Ticket, um einen Neustart des Datenintegrationsdienstes anzufordern.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Fehler beim Versuch, eine neue Tabellenzuordnung zu erstellen

**Erforderliche Anmeldeinformationen zur Behebung des Problems:** Derselbe Benutzer, der duales Schreiben eingerichtet hat.

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, eine neue Tabelle für Duales Schreiben zu konfigurieren. Der einzige Benutzer, der eine Karte erstellen kann, ist der Benutzer, der die duale Schreibverbindung eingerichtet hat.

*Der Antwortstatuscode zeigt keinen Erfolg an: 401 (Nicht erlaubt)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>Fehler beim Öffnen der Benutzeroberfläche Duales Schreiben

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, über den Arbeitsbereich **Datenmanagement** auf Duales Schreiben zuzugreifen:

*login.microsoftonline.com weigerte sich, eine Verbindung herzustellen.*

Um das Problem zu beheben, melden Sie sich über ein InPrivate-Fenster bei Microsoft Edge, ein Inkognito-Fenster in Chromium oder ein Inkognito-Fenster in Google Chrome an. Sie müssen auch Cookies von Drittanbietern entsperren oder löschen.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Fehler beim Verknüpfen der Umgebung für duales Schreiben oder Hinzufügen einer neuen Tabellenzuordnung

**Erforderliche Rolle zur Behebung des Problems:** Systemadministrator in Finance and Operations-Apps und Dataverse.

Beim Verknüpfen oder Erstellen von Zuordnungen kann der folgende Fehler auftreten:

*Antwortstatuscode zeigt keinen Erfolg an: 403 (Token-Austausch).<br> Sitzungs-ID: \<your session id\><br> Stammaktivitäts-ID: \<your root activity id\>*

Dieser Fehler kann auftreten, wenn Sie nicht über ausreichende Berechtigungen verfügen, um Duales Schreiben zu verknüpfen oder Zuordnungen zu erstellen. Dieser Fehler kann auch auftreten, wenn die Dataverse-Umgebung zurückgesetzt wurde, ohne die Verknüpfung zum dualen Schreiben aufzuheben. Jeder Benutzer mit Systemadministratorrolle in Finance and Operations-Apps und Dataverse kann die Umgebungen verbinden. Nur der Benutzer, der die duale Schreibverbindung eingerichtet hat, kann neue Tabellenzuordnungen hinzufügen. Nach dem Setup kann jeder Benutzer mit Systemadministratorrolle den Status überwachen und die Zuordnungen bearbeiten.

## <a name="error-when-you-stop-the-table-mapping"></a>Fehler beim Beenden der Tabellenzuordnung

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, die Tabellenzuordnung zu aktivieren:

*\[verboten\], \[{„Status“: 403, „Quelle“:„“,„Nachricht“:„Fehler beim Token-Austausch: Benutzer darf nicht auf die Verbindung dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx“}\] zugreifen. Der Remote-Server hat einen Fehler zurückgegeben: (403) Verboten.*

Dieser Fehler tritt auf, wenn die verknüpfte Dataverse Umgebung nicht verfügbar ist.

Erstellen Sie ein Ticket für das Datenintegrationsteam, um das Problem zu beheben. Fügen Sie die Netzwerkablaufverfolgung hinzu, damit das Datenintegrationsteam die Zuordnung als **wird nicht ausgeführt** im hinteren Ende markieren kann.

## <a name="error-while-trying-to-start-a-table-mapping"></a>Fehler beim Versuch, eine Tabellenzuordnung zu starten

Möglicherweise wird eine Fehlermeldung wie die folgende angezeigt, wenn Sie versuchen, den Status einer Zuordnung auf **Laufend** festzulegen:

*Die anfängliche Datensynchronisierung kann nicht abgeschlossen werden. Fehler: Dualer Schreibfehler – Plugin-Registrierung fehlgeschlagen: Suchmetadaten für duales Schreiben können nicht erstellt werden. Fehlerobjektreferenz nicht auf eine Instanz eines Objekts festgelegt.*

Die Behebung dieses Fehlers hängt von der Fehlerursache ab:

+ Wenn die Zuordnung abhängige Zuordnungen enthält, müssen Sie die abhängigen Zuordnungen dieser Tabellenzuordnung aktivieren.
+ In der Zuordnung fehlen möglicherweise Quell- oder Zielspalten. Wenn eine Spalte in der Finance and Operations-App fehlt, dann befolgen Sie die Schritte im Abschnitt [Fehlende Tabellenspalten treten in Zuordnungen auf](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps). Wenn eine Spalte in Dataverse fehlt, klicken Sie in der Zuordnung auf die Schaltfläche **Tabellen aktualisieren**, damit die Spalten automatisch wieder in die Zuordnung eingefügt werden.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]