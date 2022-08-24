---
title: Probleme bei der anfänglichen Einrichtung behandeln
description: Dieser Artikel enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Einrichtung der Integration vom dualen Schreiben zusammenhängen.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d33fc6f4895b53f16cc6957a3a2fc6b1abe90a2f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289513"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Probleme bei der anfänglichen Einrichtung behandeln

[!include [banner](../../includes/banner.md)]

Dieser Artikel enthält Informationen zur Problembehandlung für die Dual-write Integration zwischen Finanz- und Betriebs-Apps und Dataverse. Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Einrichtung der Integration vom dualen Schreiben zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Artikel behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD)-Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Sie können eine Finanz- und Betriebs-App nicht mit Dataverse verknüpfen.

**Benötigte Rolle, um Dual-write festzulegen:** Systemadministrator in den Finanz- und Betriebs-Apps und Dataverse.

Fehler auf der Seite **Einrichtungs-Link für Dataverse** werden normalerweise durch unvollständige Setup- oder Berechtigungsprobleme verursacht. Stellen Sie sicher, dass die gesamte Integritätsprüfung die Seite **Einrichtungs-Link zu Dataverse** wie in der folgenden Abbildung gezeigt. Sie können Duales Schreiben nur verknüpfen, wenn die gesamte Integritätsprüfung bestanden wurde.

![Erfolgreiche Integritätsprüfung.](media/health_check.png)

Sie müssen über Azure AD Mandant-Admin-Anmeldeinformationen verfügen, um die Finanzen und Betrieb und Dataverse Umgebungen zu verknüpfen. Nachdem Sie die Umgebungen verknüpft haben, können sich Benutzer mit ihren Kontoanmeldeinformationen anmelden und eine vorhandene Tabellenzuordnung aktualisieren.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Finden Sie das Limit für die Anzahl der juristischen Tabellen oder Unternehmen, die für duales Schreiben verknüpft werden können

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, die Zuordnung zu aktivieren:

*Dual Write Fehler - Plugin-Registrierung fehlgeschlagen: [(Partitionszuordnung für Projekt DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea kann nicht zugewiesen werden. Fehler Überschreitet die maximal zulässigen Partitionen für die Zuordnung DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], Ein oder mehrere Fehler sind aufgetreten.*

Die aktuelle Limite beim Verknüpfen der Umgebungen beträgt ungefähr 40 juristische Tabellen. Dieser Fehler tritt auf, wenn Sie versuchen, Karten zu aktivieren, und mehr als 40 juristische Tabellen zwischen den Umgebungen verknüpft sind.

## <a name="connection-set-failed-while-linking-environment"></a>Beim Verknüpfen der Umgebung konnte die Verbindung nicht festgelegt werden

Während der Verknüpfung der Dual-Write-Umgebung schlägt die Aktion mit einer Fehlermeldung fehl:

*Speichern des Verbindungssatzes fehlgeschlagen! Es wurde bereits ein Element mit demselben Schlüssel hinzugefügt.*

Dual-Write unterstützt nicht mehrere juristische Entitäten/Firmen mit demselben Namen. Wenn Sie z. B. zwei Firmen mit dem Namen „DAT“ in der Dataverse haben, dann wird diese Fehlermeldung ausgegeben.

Um den Debitor zu entsperren, entfernen Sie doppelte Datensätze aus der Tabelle **cdm_company** in der Dataverse. Wenn die Tabelle **cdm_company** außerdem Datensätze mit leerem Namen enthält, entfernen oder korrigieren Sie diese Datensätze.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Fehler beim Öffnen der Dual-write Seite in Finanz- und Betriebs-Apps

Möglicherweise erhalten Sie die folgende Fehlermeldung, wenn Sie versuchen, eine Dataverse-Umgebung für Dual-write zu verknüpfen:

*Der Antwortstatuscode zeigt keinen Erfolg an: 404 (Nicht gefunden).*

Dieser Fehler tritt auf, wenn der Schritt der App-Zustimmung nicht vollständig ist. Sie können überprüfen, ob die Zustimmung erteilt wurde, indem Sie sich mit dem Mandant-Admin-Konto bei `portal.azure.com` anmelden und prüfen, ob die App eines Drittanbieters mit der ID `33976c19-1db5-4c02-810e-c243db79efde` in der Liste der Enterprise-Anwendungen von AAD auftaucht. Wenn nicht, dann wiederholen Sie den Schritt der Zustimmung wie im nächsten Abschnitt beschrieben.

### <a name="providing-app-consent"></a>Zustimmung zur App erteilen

+ Starten Sie die folgende URL mit Ihren Admin-Anmeldeinformationen.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Wählen Sie **Akzeptieren**, um zuzustimmen. Sie erteilen damit die Zustimmung zur Installation der App (mit `id=33976c19-1db5-4c02-810e-c243db79efde`) in Ihrem Mandant.
+ Diese App wird benötigt, damit Dataverse mit den Finanz- und Betriebs-Apps kommunizieren kann.

    ![Problembehandlung bei der ersten Einrichtung der Synchronisierung.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Wenn dies nicht funktioniert, starten Sie die URL im privaten Modus von Microsoft Edge oder im Inkognito-Modus von Chrome .

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Finanz- und Betriebs-Umgebung ist nicht auffindbar

Möglicherweise erhalten Sie die folgende Fehlermeldung:

*Finanz- und Betriebs-Apps Umgebung \*\*\*.cloudax.dynamics.com ist nicht auffindbar.*

Es gibt zwei Dinge, die ein Problem mit nicht auffindbarer Umgebung verursachen können:

+ Der Benutzer, der für die Anmeldung verwendet wird, befindet sich nicht im selben Mandanten wie die Finanzen und Betrieb-Instanz.
+ Es gibt einige veraltete Finanzen und Betrieb-Instanzen, die von Microsoft gehostet wurden und bei denen es ein Problem mit der Erkennung gab. Um dies zu beheben, aktualisieren Sie die Finanzen und Betrieb-Instanz. Die Umgebung wird mit jeder Aktualisierung auffindbar.

## <a name="403-forbidden-error-while-connections-are-being-created"></a>403 (Nicht zulässig) Fehler beim Erstellen von Verbindungen

Als Teil des Verknüpfungsprozesses zum dualen Schreiben werden zwei Power Apps Verbindungen (auch bekannt als *Apihub* Verbindungen) werden im Namen des Benutzers in der verlinkten Dataverse Umgebung erstellt. Wenn der Kunde keine Lizenz für die Power Apps-Umgebung hat, schlägt die Erstellung der ApiHub-Verbindungen fehl und ein 403-Fehler (nicht zulässig) wird angezeigt. Hier ist ein Beispiel für die Fehlernachricht:

> MSG=\[Umgebung für duales Schreiben konnte nicht eingerichtet werden. Fehlerdetails: Antwort-Statuscode zeigt keinen Erfolg an: 403 (nicht zulässig). - Der Antwortstatuscode zeigt keinen Erfolg an: 403 (nicht zulässig).\] STAPELÜBERWACHUNG=\[   bei Microsoft.Dynamics.Integrator.ProjectManagementService.DualWrite.DualWriteConnectionSetProcessor.\<CreateDualWriteConnectionSetAsync\>d\_\_29.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\DualWrite\\DualWriteConnectionSetProcessor.cs:line 297 --- Ende der Stapelüberwachung vom vorherigen Speicherort, an dem die Ausnahme ausgelöst wurde --- bei System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw() bei System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task) bei Microsoft.Dynamics.Integrator.ProjectManagementService.Controllers.DualWriteEnvironmentManagementController.\<SetupDualWriteEnvironmentAsync\>d\_\_34.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\Controllers\\DualWriteEnvironmentManagementController.cs:line 265\]

Dieser Fehler tritt auf, weil keine Power Apps-Lizenz vorliegt. Weisen Sie dem Benutzer eine entsprechende Lizenz zu (z. B. Power Apps Test 2 Plan), damit der Benutzer die Berechtigung zum Erstellen der Verbindungen hat. Um die Lizenz zu überprüfen, kann der Kunde zur Website [Mein Konto](https://portal.office.com/account/?ref=MeControl#subscriptions) gehen, um die Lizenzen anzuzeigen, die dem Benutzer derzeit zugewiesen sind.

Weitere Informationen zu Power Apps-Lizenzen finden Sie in den folgenden Artikeln:

- [Benutzern Lizenzen zuweisen](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide)
- [Power Apps für Ihre Organisation kaufen](/power-platform/admin/signup-for-powerapps-admin)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

