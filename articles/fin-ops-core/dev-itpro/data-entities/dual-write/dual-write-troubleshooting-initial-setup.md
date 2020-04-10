---
title: Probleme bei der anfänglichen Einrichtung behandeln
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die bei der Ersteinrichtung der Dual-Write-Integration zwischen Finance and Operations Apps und Common Data Service auftreten können.
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
ms.openlocfilehash: e20c9c5e1250c8e65b5642a7c45d7ae859315697
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172667"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Probleme bei der anfänglichen Einrichtung behandeln

[!include [banner](../../includes/banner.md)]



Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Common Data Service. Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Einrichtung der Integration vom dualen Schreiben zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a>Sie können eine Finance and Operations App nicht mit Common Data Service verknüpfen

**Erforderliche Anmeldeinformationen zum Einrichten von Dualem Schreiben:** Azure AD Mandant Admin

Fehler auf der Seite **Einrichtungs-Link für Common Data Service** werden normalerweise durch unvollständige Setup- oder Berechtigungsprobleme verursacht. Stellen Sie sicher, dass die gesamte Integritätsprüfung die Seite **Einrichtungs-Link zu Common Data Service** wie in der folgenden Abbildung gezeigt. Sie können Duales Schreiben nur verknüpfen, wenn die gesamte Integritätsprüfung bestanden wurde.

![Erfolgreiche Integritätsprüfung](media/health_check.png)

Sie müssen Azure AD Mandantenadministrator-Anmeldeinformationen haben, um Finance and Operations und Common Data Service Umgebungen zu verknüpfen. Nachdem Sie die Umgebungen verknüpft haben, können sich Benutzer mit ihren Kontoanmeldeinformationen anmelden und eine vorhandene Entitätszuordnung aktualisieren.

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a>Fehler beim Öffnen des Links zur Seite Common Data Service

**Erforderliche Anmeldeinformationen zum Lösen des Problems:** Azure AD Mandant Admin

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie den **Link zur Common Data Service** Seite in einer Finance and Operations App öfnen:

*Der Antwortstatuscode zeigt keinen Erfolg an: 404 (Nicht gefunden).*

Dieser Fehler tritt auf, wenn der Zustimmungsschritt nicht abgeschlossen wurde. Melden Sie sich bei Portal.Azure.com an, um zu überprüfen, ob der Zustimmungsschritt abgeschlossen wurde mithilfe dem Azure AD Mandantenadministratorkonto, und prüfen Sie, ob die Drittanbieter-App die über die ID verfügt **33976c19-1db5-4c02-810e-c243db79efde** in der Azure AD **Unternehmensanwendungen** angezeigt wird. Wenn dies nicht der Fall ist, müssen Sie die Zustimmung der App geben.

Führen Sie die folgenden Schritte aus, um die App-Zustimmung zu erteilen.

1. Öffnen Sie die folgende URL mithilfe Ihrer Administratoranmeldeinformationen. Sie sollten zur Zustimmung aufgefordert werden.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Wählen **Akzeptieren**, um anzugeben, dass Sie Ihre Zustimmung zur Installation der App mit der ID **33976c19-1db5-4c02-810e-c243db79efde** in Ihrem Mandant geben.

    > [!TIP]
    > Diese App muss verlinkt werden mit Common Data Service und Finance and Operations Apps. Wenn Sie Probleme mit diesem Schritt haben, öffnen Sie Ihren Browser im Inkognito-Modus (in Google Chrome) oder im InPrivate-Modus (in Microsoft Edge).

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Stellen Sie sicher, dass Unternehmensdaten und Teams Duales Schreiben während der Verknüpfung korrekt eingerichtet sind

Um sicherzustellen, dass Duales Schreiben ordnungsgemäß funktioniert, werden die Unternehmen, die Sie während der Konfiguration auswählen, in der Liste Common Data Service Umgebung erstellt. Standardmäßig sind diese Unternehmen schreibgeschützt und die **IsDualWriteEnable** Eigenschaft ist auf **Wahr** festgelegt. Darüber hinaus werden der Eigentümer und das Team der Geschäftseinheit mit Standardbesitz erstellt und enthalten den Firmennamen. Stellen Sie vor dem Aktivieren der Karten sicher, dass der Standardteambesitzer angegeben ist. Um **Unternehmen (CDM\_Unternehmen)** Entität zu finden, folgen Sie diesen Schritten.

1. Wählen Sie in der modellgesteuerten App in Dynamics 365 den Filter in der oberen rechten Ecke aus.
2. Wählen Sie in der Dropdownliste **Unternehmen** aus.
3. Wählen **Ausführen**, um die Ergebnisse zu sehen.
4. Wählen Sie die Firma aus, die bei der Konfiguration von Dualem Schreiben verknüpft war.
5. Stellen Sie sicher, dass das Feld **Standardbesitzerteam** einen Wert hat. In der folgenden Abbildung ist das Feld **Standardbesitzerteam** auf **USMF – Duales Schreiben** festgelegt.

    ![Überprüfen des Standardbesitzerteams](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a>Finden Sie das Limit für die Anzahl der juristischen Personen oder Unternehmen, die für Duales Schreiben verknüpft werden können

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, die Zuordnung zu aktivieren:

*Dualer Schreibfehler – Plugin-Registrierung fehlgeschlagen: \[(Partitionszuordnung für Projekt DWM kann nicht abgerufen werden-1ae35e60-4bc2-4905-88ea-69efd3b29260–7f12cb89-1550-42e2-858e-4761fc1443ea . Fehler überschreitet die maximal zulässigen Partitionen für die Zuordnung von DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260–7f12cb89-1550-42e2-858e-4761fc1443ea)\]Ein oder mehrere Fehler sind aufgetreten.*

Die aktuelle Limite beim Verknüpfen der Umgebungen beträgt ungefähr 40 juristische Personen. Dieser Fehler tritt auf, wenn Sie versuchen, Karten zu aktivieren, und mehr als 40 juristische Personen zwischen den Umgebungen verknüpft sind.
