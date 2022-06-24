---
title: Probleme bei der anfänglichen Einrichtung behandeln
description: Dieser Artikel enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Einrichtung der Integration vom dualen Schreiben zusammenhängen.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 5ebb14dad723fad5b17b4dfca153bf153e77bbd4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882083"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Probleme bei der anfänglichen Einrichtung behandeln

[!include [banner](../../includes/banner.md)]



Dieser Artikel enthält Informationen zur Problembehandlung für die Integration von dualem Schreiben zwischen Finanz- und Betriebs-Apps und Dataverse. Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Einrichtung der Integration vom dualen Schreiben zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Artikel behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD)-Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Sie können eine Finance und Operations App nicht mit Dataverse verknüpfen.

**Benötigte Rolle, um duales Schreiben festzulegen:** Systemadministrator in den Apps Finance und Operations und Dataverse.

Fehler auf der Seite **Einrichtungs-Link für Dataverse** werden normalerweise durch unvollständige Setup- oder Berechtigungsprobleme verursacht. Stellen Sie sicher, dass die gesamte Integritätsprüfung die Seite **Einrichtungs-Link zu Dataverse** wie in der folgenden Abbildung gezeigt. Sie können Duales Schreiben nur verknüpfen, wenn die gesamte Integritätsprüfung bestanden wurde.

![Erfolgreiche Integritätsprüfung.](media/health_check.png)

Sie müssen über Anmeldeinformationen für Azure AD Mandant verfügen, um die Umgebungen Finance und Operations und Dataverse zu verknüpfen. Nachdem Sie die Umgebungen verknüpft haben, können sich Benutzer mit ihren Kontoanmeldeinformationen anmelden und eine vorhandene Tabellenzuordnung aktualisieren.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Finden Sie das Limit für die Anzahl der juristischen Tabellen oder Unternehmen, die für duales Schreiben verknüpft werden können

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, die Zuordnung zu aktivieren:

*Dual Write Fehler - Plugin-Registrierung fehlgeschlagen: [(Partitionszuordnung für Projekt DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea kann nicht zugewiesen werden. Fehler Überschreitet die maximal zulässigen Partitionen für die Zuordnung DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], Ein oder mehrere Fehler sind aufgetreten.*

Die aktuelle Limite beim Verknüpfen der Umgebungen beträgt ungefähr 40 juristische Tabellen. Dieser Fehler tritt auf, wenn Sie versuchen, Karten zu aktivieren, und mehr als 40 juristische Tabellen zwischen den Umgebungen verknüpft sind.

## <a name="connection-set-failed-while-linking-environment"></a>Beim Verknüpfen der Umgebung konnte die Verbindung nicht festgelegt werden

Während der Verknüpfung der Dual-Write-Umgebung schlägt die Aktion mit einer Fehlermeldung fehl:

*Speichern des Verbindungssatzes fehlgeschlagen! Es wurde bereits ein Element mit demselben Schlüssel hinzugefügt.*

Dual-Write unterstützt nicht mehrere juristische Entitäten/Firmen mit demselben Namen. Wenn Sie z.B. zwei Firmen mit dem Namen "DAT" in der Dataverse haben, dann wird diese Fehlermeldung ausgegeben.

Um den Debitor zu entsperren, entfernen Sie doppelte Datensätze aus der Tabelle **cdm_company** in der Dataverse. Wenn die Tabelle **cdm_company** außerdem Datensätze mit leerem Namen enthält, entfernen oder korrigieren Sie diese Datensätze.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Fehler beim Öffnen der duales Schreiben Seite in Apps für Finanzen und Betrieb

Möglicherweise erhalten Sie die folgende Fehlermeldung, wenn Sie versuchen, eine Dataverse-Umgebung für Dual-write zu verknüpfen:

*Der Antwortstatuscode zeigt keinen Erfolg an: 404 (Nicht gefunden).*

Dieser Fehler tritt auf, wenn der Schritt der App-Zustimmung nicht vollständig ist. Sie können überprüfen, ob die Zustimmung erteilt wurde, indem Sie sich mit dem Mandant-Admin-Konto bei `portal.azure.com` anmelden und prüfen, ob die App eines Drittanbieters mit der ID `33976c19-1db5-4c02-810e-c243db79efde` in der Liste der Enterprise-Anwendungen von AAD auftaucht. Wenn nicht, dann wiederholen Sie den Schritt der Zustimmung wie im nächsten Abschnitt beschrieben.

### <a name="providing-app-consent"></a>Zustimmung zur App erteilen

+ Starten Sie die folgende URL mit Ihren Admin-Anmeldeinformationen.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Wählen Sie **Akzeptieren**, um zuzustimmen. Sie erteilen damit die Zustimmung zur Installation der App (mit `id=33976c19-1db5-4c02-810e-c243db79efde`) in Ihrem Mandant.
+ Diese App ist für Dataverse erforderlich, um mit Apps für Finanzen und Betrieb zu kommunizieren.

    ![Problembehandlung bei der ersten Einrichtung der Synchronisierung.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Wenn dies nicht funktioniert, starten Sie die URL im privaten Modus von Microsoft Edge oder im Inkognito-Modus von Chrome .

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Die Umgebung von Finance und Operations ist nicht auffindbar.

Möglicherweise erhalten Sie die folgende Fehlermeldung:

*Umgebung der Apps für Finance und Operations \*\*\*.cloudax.dynamics.com ist nicht auffindbar.*

Es gibt zwei Dinge, die ein Problem mit nicht auffindbarer Umgebung verursachen können:

+ Der für die Anmeldung verwendete Benutzer befindet sich nicht im selben Mandanten wie die Finance und Operations-Instanz.
+ Es gibt einige veraltete Finance und Operations-Instanzen, die von Microsoft gehostet wurden und bei denen es ein Problem mit der Erkennung gab. Um das Problem zu beheben, aktualisieren Sie die Finance und Operations-Instanz. Die Umgebung wird mit jeder Aktualisierung auffindbar.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
