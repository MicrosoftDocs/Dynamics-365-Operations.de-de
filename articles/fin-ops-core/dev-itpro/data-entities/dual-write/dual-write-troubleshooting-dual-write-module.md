---
title: Problembehandlung von Dual-write-Problemen in Finanz- und Betriebs-Apps
description: Dieser Artikel enthält Informationen zur Problembehandlung, die Ihnen helfen können, Probleme mit dem Dual-write-Modul in Finanz- und Betriebs-Apps zu beheben.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 5678cd38e48eb5226e36851679436d3b6c117cf9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289573"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Problembehandlung von Dual-write-Problemen in Finanz- und Betriebs-Apps

[!include [banner](../../includes/banner.md)]



Dieser Artikel enthält Informationen zur Problembehandlung für die Dual-write Integration zwischen Finanz- und Betriebs-Apps und Dataverse. Insbesondere liefert es Informationen, die Ihnen helfen können, Probleme mit dem **Dual-write** Modul in Finanz- und Betriebs-Apps zu beheben.

> [!IMPORTANT]
> Einige der in diesem Artikel behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD)-Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Sie können das Dual-write Modul nicht in eine Finanz- und Betriebs-App laden

Wenn Sie die Seite **Duales Schreiben** nicht öffnen können durch Auswahl der Kachel **Duales Schreiben** im Arbeitsbereich **Datenmverwaltung**, ist der Datenintegrationsdienst wahrscheinlich ausgefallen. Erstellen Sie ein Support-Ticket, um einen Neustart des Datenintegrationsdienstes anzufordern.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Fehler beim Versuch, eine neue Tabellenzuordnung zu erstellen

**Erforderliche Anmeldeinformationen zur Behebung des Problems:** Derselbe Benutzer, der duales Schreiben eingerichtet hat.

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, eine neue Tabelle für Duales Schreiben zu konfigurieren. Der einzige Benutzer, der eine Karte erstellen kann, ist der Benutzer, der die duale Schreibverbindung eingerichtet hat.

*Antwort-Statuscode zeigt keinen Erfolg an: 401 (Unautorisiert).*

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Fehler beim Öffnen der Benutzeroberfläche Duales Schreiben

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, über den Arbeitsbereich **Datenmanagement** auf Duales Schreiben zuzugreifen:

*login.microsoftonline.com weigerte sich, eine Verbindung herzustellen.*

Um das Problem zu beheben, melden Sie sich über ein InPrivate-Fenster bei Microsoft Edge, ein Inkognito-Fenster in Chromium oder ein Inkognito-Fenster in Google Chrome an. Sie müssen auch Cookies von Drittanbietern entsperren oder löschen.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Fehler beim Verknüpfen der Umgebung für duales Schreiben oder Hinzufügen einer neuen Tabellenzuordnung

**Erforderliche Rolle, um das Problem zu beheben:** Systemadministrator in den Finanz- und Betriebs-Apps und Dataverse.

Beim Verknüpfen oder Erstellen von Zuordnungen kann der folgende Fehler auftreten:

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

Dieser Fehler kann auftreten, wenn Sie nicht über ausreichende Berechtigungen verfügen, um Duales Schreiben zu verknüpfen oder Zuordnungen zu erstellen. Dieser Fehler kann auch auftreten, wenn die Dataverse-Umgebung zurückgesetzt wurde, ohne die Verknüpfung zum dualen Schreiben aufzuheben. Jeder Benutzer mit der Systemadministratorrolle in den Apps Finanzen und Betrieb und Dataverse kann die Umgebungen miteinander verbinden. Nur der Benutzer, der die duale Schreibverbindung eingerichtet hat, kann neue Tabellenzuordnungen hinzufügen. Nach dem Setup kann jeder Benutzer mit Systemadministratorrolle den Status überwachen und die Zuordnungen bearbeiten.

## <a name="error-when-you-stop-the-table-mapping"></a>Fehler beim Beenden der Tabellenzuordnung

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, die Tabellenzuordnung zu aktivieren:

*\[verboten\], \[{„Status“: 403, „Quelle“:„“,„Nachricht“:„Fehler beim Token-Austausch: Benutzer darf nicht auf die Verbindung dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx“}\] zugreifen. Der Remote-Server hat einen Fehler zurückgegeben: (403) Verboten.*

Dieser Fehler tritt auf, wenn die verknüpfte Dataverse Umgebung nicht verfügbar ist.

Erstellen Sie ein Ticket für das Datenintegrationsteam, um das Problem zu beheben. Fügen Sie die Netzwerkablaufverfolgung hinzu, damit das Datenintegrationsteam die Zuordnung als **wird nicht ausgeführt** im hinteren Ende markieren kann.

## <a name="enable-parallel-processing-in-finance-and-operations-apps-to-improve-performance"></a>Ermöglichen Sie die parallele Verarbeitung in Finanz- und Betriebs-Apps, um die Leistung zu verbessern.

Durch die Aktivierung der parallelen Verarbeitung kann der Zeitaufwand für den Import von Daten aus Dynamics 365 Customer Engagement-Apps und Microsoft Dataverse in Finanz- und Betriebs-Apps verringert werden. 

Um die parallele Verarbeitung in Finanz- und Betriebs-Apps zu aktivieren, führen Sie die folgenden Schritte aus.

1. Melden Sie sich in Ihrer Finanz- und Betriebs-Umgebung an.
2. Wechseln Sie zu **Datenverwaltung > Frameworkparameter**.
3. Wählen Sie **Entitätseinstellungen** und dann **Entitätsausführungsparameter konfigurieren** aus.
4. Fügen Sie die Parameter für die parallele Verarbeitung hinzu:
    - **Importschwellendatensatz-Zählung** – Die Anzahl der Datensätze, die erreicht sein muss, bevor die Parallelverarbeitung aktiviert wird.
    - **Importaufgabenzählung** – Die Anzahl der Threads (Aufgaben), die parallel ausgeführt werden sollen.
5. Wählen Sie **Speichern** aus.


## <a name="errors-while-trying-to-start-a-table-mapping"></a>Fehler beim Versuch, eine Tabellenzuordnung zu starten

### <a name="unable-to-complete-initial-data-sync"></a>Die anfängliche Datensynchronisation konnte nicht abgeschlossen werden

Möglicherweise erhalten Sie einen Fehler wie den folgenden, wenn Sie versuchen, die anfängliche Datensynchronisierung auszuführen:

*Die anfängliche Datensynchronisierung kann nicht abgeschlossen werden. Fehler: Dualer Schreibfehler – Plugin-Registrierung fehlgeschlagen: Suchmetadaten für duales Schreiben können nicht erstellt werden. Fehlerobjektreferenz nicht auf eine Instanz eines Objekts festgelegt.*

Wenn Sie versuchen, den Status einer Zuordnung auf **Laufend** festzulegen, erhalten Sie möglicherweise diesen Fehler. Die Behebung hängt von der Ursache des Fehlers ab:

+ Wenn die Zuordnung abhängige Zuordnungen enthält, müssen Sie die abhängigen Zuordnungen dieser Tabellenzuordnung aktivieren.
+ In der Zuordnung fehlen möglicherweise Quell- oder Zielspalten. Wenn eine Spalte in der Finanz- und Betriebs-App fehlt, befolgen Sie die Schritte im Abschnitt [Fehlende Tabellenspalten auf Maps](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps). Wenn eine Spalte in Dataverse fehlt, klicken Sie in der Zuordnung auf die Schaltfläche **Tabellen aktualisieren**, damit die Spalten automatisch wieder in die Zuordnung eingefügt werden.

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>Fehler bei der Versionsübereinstimmung und Upgrade von Dual-Write-Lösungen

Möglicherweise erhalten Sie folgende Fehlermeldungen, wenn Sie versuchen, die Zuordnungen der Tabellen auszuführen:

+ *Kundengruppen (msdyn_customergroups) : Dual-Write-Fehler - Dynamics 365 for Sales Lösung 'Dynamics365Company' hat eine Versionsabweichung. Version: '2.0.2.10' Erforderliche Version: '2.0.133'*
+ *Dynamics 365 for Sales Lösung 'Dynamics365FinanceExtended' hat Versionsabweichung. Version: '1.0.0.0' Erforderliche Version: '2.0.227'*
+ *Dynamics 365 for Sales Lösung 'Dynamics365FinanceAndOperationsCommon' hat Versionsinkongruenz. Version: '1.0.0.0' Erforderliche Version: '2.0.133'*
+ *Dynamics 365 for Sales Lösung 'CurrencyExchangeRates' hat eine Versionsabweichung. Version: '1.0.0.0' Erforderliche Version: '2.0.133'*
+ *Dynamics 365 for Sales Lösung 'Dynamics365SupplyChainExtended' hat eine Versionsabweichung. Version: '1.0.0.0' Erforderliche Version: '2.0.227'*

Um die Probleme zu beheben, aktualisieren Sie die Dual-Write-Lösungen in Dataverse. Stellen Sie sicher, dass Sie auf die neueste Lösung aktualisieren, die mit der erforderlichen Lösungsversion übereinstimmt.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

