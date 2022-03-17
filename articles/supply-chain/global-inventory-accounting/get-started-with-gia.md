---
title: Einstieg in die Globale Bestandsbuchhaltung
description: In diesem Thema wird beschrieben, wie Sie mit der Globalen Bestandsbuchhaltung loslegen.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88f1e9ef8c8b2aa494c44ea3b33713adc470eb96
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384796"
---
# <a name="get-started-with-global-inventory-accounting"></a>Einstieg in die Globale Bestandsbuchhaltung

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Mit der Globalen Bestandsbuchhaltung können Sie mehrere Bestandsbuchhaltungen in den von Ihnen festgelegten Sachkonten der Globalen Bestandsbuchhaltung durchführen. Sie müssen jedes Sachkonto der Globalen Bestandsbuchhaltung mit einer *Konvention* verknüpfen. Eine Konvention ist eine Sammlung der folgenden Arten von Rechnungslegungsgrundsätzen:

- Kostenobjekt
- Messungsgrundlage für Eingabe
- Kostenflussannahme
- Kostenelement

> [!NOTE]
> Auch nachdem Sie die Globale Bestandsbuchhaltung eingeschaltet haben, können Sie die Bestandsbuchhaltung in Microsoft Dynamics 365 Supply Chain Management wie gewohnt durchführen.

Die Globale Bestandsbuchhaltung ist ein Add-In. Um seine Funktionen verfügbar zu machen, müssen Sie es über die Microsoft Dynamics Lifecycle Services (LCS) installieren. Sie können es in einer Testumgebung testen, bevor Sie es für Produktionsumgebungen einschalten.

Die Globale Bestandsbuchhaltung unterstützt derzeit nicht alle Funktionen der Kostenverwaltung, die in Supply Chain Management integriert sind. Daher ist es wichtig, dass Sie prüfen, ob der derzeit verfügbare Funktionsumfang Ihren Anforderungen entspricht.

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a>Wie Sie die öffentliche Vorschau der Globalen Bestandsbuchhaltung erhalten

> [!IMPORTANT]
> Um die Globale Bestandsbuchhaltung zu verwenden, müssen Sie über eine LCS-fähige Hochverfügbarkeitsumgebung verfügen (keine OneBox-Umgebung). Außerdem müssen Sie Supply Chain Management Version 10.0.19 oder höher ausführen.

Um sich für die öffentliche Vorschau der Globalen Bestandsbuchhaltung anzumelden, senden Sie Ihre LCS Umgebungs-ID per E-Mail an das [Globale Bestandsbuchhaltung Team](mailto:GlobalInvAccount@microsoft.com). Nachdem Sie für das Programm genehmigt wurden, sendet Ihnen das Team eine Nachverfolgungs-E-Mail, die einen Beta-Schlüssel für die Globale Bestandsbuchhaltung und Ihre Service-Endpunkte enthält. Nachdem Sie den Beta-Schlüssel erhalten haben, können Sie [das Add-In installieren](#install).

## <a name="licensing"></a>Lizenzierung

Globale Bestandsbuchhaltung wird zusammen mit den Standardfunktionen der Bestandsbuchhaltung lizenziert, die für Supply Chain Management verfügbar sind. Sie müssen keine zusätzliche Lizenz kaufen, um die Globale Bestandsbuchhaltung zu nutzen.

## <a name="prerequisites"></a>Voraussetzungen

### <a name="set-up-microsoft-power-platform-integration"></a>Microsoft Power Platform-Integration einrichten

Bevor Sie die Add-In-Funktionalität aktivieren können, müssen Sie die Microsoft Power Platform-Integration durchführen, indem Sie die folgenden Schritte ausführen.

1. Öffnen Sie die LCS-Umgebung, in der Sie den Dienst hinzufügen möchten.
1. Gehen Sie zu **Vollständige Details**.
1. Wählen Sie im Abschnitt **Power Platform-Integration** die Option **Einrichten** aus.
1. Aktivieren Sie im Dialogfeld **Einrichten der Power Platform Umgebung** das Kontrollkästchen und wählen Sie dann **Einrichten**. In der Regel dauert das Einrichten zwischen 60 und 90 Minuten.
1. Nachdem das Einrichten der Microsoft Power Platform-Umgebung abgeschlossen ist, wird auf der Seite der Name Ihrer Umgebung angezeigt. Außerdem wird im Abschnitt **Power Platform-Integration** die Aussage „Power Platform-Umgebung einrichten ist abgeschlossen.“ Für die Globale Bestandsbuchhaltung ist keine Dual-Write-Anwendung erforderlich.

Weitere Informationen finden Sie unter [Nach Bereitstellen der Umgebung aktivieren](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy).

### <a name="set-up-dataverse"></a>Dataverse einrichten

Bevor Sie Dataverse festlegen, fügen Sie die Serviceprinzipien der Globalen Bestandsbuchhaltung zu Ihrem Mandant hinzu, indem Sie die folgenden Schritte ausführen.

1. Installieren Sie Azure AD Modul für Windows PowerShell v2 wie in [Installieren von Azure Active Directory PowerShell für Graph](/powershell/azure/active-directory/install-adv2) beschrieben.
1. Führen Sie den folgenden PowerShell-Befehl aus.

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

Erstellen Sie anschließend Anwendungsbenutzer für die Globale Bestandsbuchhaltung in Dataverse, indem Sie die folgenden Schritte ausführen.

1. Öffnen Sie die URL Ihrer Dataverse-Umgebung.
1. Gehen Sie zu **Erweiterte Einstellung \> System \> Sicherheit \> Benutzer**, und erstellen Sie einen Anwendungsbenutzer. Verwenden Sie das Feld **Ansicht**, um die Seitenansicht auf *Anwendungsbenutzer* zu ändern.
1. Wählen Sie **Neu** aus.
1. Legen Sie das Feld **Anwendungs-ID** auf *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9* fest.
1. Wählen Sie **Rolle zuweisen**, und wählen Sie dann *Systemadministrator*. Wenn es eine Rolle gibt, die *Common Data Service Benutzer* heißt, wählen Sie diese ebenfalls aus.
1. Wiederholen Sie die vorangegangenen Schritte, aber legen Sie das Feld **Anwendungs-ID** auf *5f58fc56-0202-49a8-ac9e-0946b049718b* fest.

Weitere Informationen finden Sie unter [Erstellen eines Anwendungsbenutzers](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

Wenn die Standardsprache Ihrer Dataverse-Installation nicht Englisch ist, gehen Sie wie folgt vor.

1. Gehen Sie zu **Erweiterte Einstellung \> Verwaltung \> Sprachen**.
1. Wählen Sie *Englisch* (*LanguageCode=1033*), und wählen Sie dann **Anwenden**.

## <a name="install-the-add-in"></a><a name="install"></a>Installieren des Add-Ins

Gehen Sie folgendermaßen vor, um das Add-In zu installieren, damit Sie die Globale Bestandsbuchhaltung verwenden können.

1. [Melden Sie sich](#sign-up) für die öffentliche Vorschau der Globalen Bestandsbuchhaltung an.
1. Melden Sie sich bei [LCS](https://lcs.dynamics.com/Logon/Index) an.
1. Navigieren Sie zu **Verwaltung von Vorschaufunktionen**.
1. Wählen Sie das Pluszeichen (**+**).
1. Geben Sie in das Feld **Code** Ihren Add-In-Betaschlüssel für die Globale Bestandsbuchhaltung ein. (Sie sollten Ihren Beta-Schlüssel per E-Mail erhalten haben, als Sie sich angemeldet haben.)
1. Wählen Sie **Entsperren** aus.
1. Öffnen Sie die LCS-Umgebung, in der Sie den Dienst hinzufügen möchten.
1. Gehen Sie zu **Vollständige Details**.
1. Gehen Sie zu **Power Platform Integration**, und wählen Sie **Einrichten**.
1. Aktivieren Sie im Dialogfeld **Einrichten der Power Platform Umgebung** das Kontrollkästchen und wählen Sie dann **Einrichten**. In der Regel dauert das Einrichten zwischen 60 und 90 Minuten.
1. Nach dem Einrichten der Microsoft Power Platform-Umgebung wählen Sie auf dem Inforegister **Umgebungs-Add-Ins** die Option **Ein neues Add-In installieren**.
1. Wählen Sie **Globale Bestandsbuchhaltung**.
1. Befolgen Sie die Installationsanleitung und erklären Sie sich mit den Allgemeinen Geschäftsbedingungen einverstanden.
1. Wählen Sie **Installieren**.
1. Auf der Registerkarte **Umgebungs-Add-Ins** Inforegister sollten Sie sehen, dass Globale Bestandsbuchhaltung installiert wird. Nach einigen Minuten sollte sich der Status von *Installieren* in *Installiert* ändern. (Möglicherweise müssen Sie die Seite aktualisieren, um diese Änderung zu sehen.) An diesem Punkt ist die Globale Bestandsbuchhaltung einsatzbereit.

## <a name="set-up-the-integration"></a>Einrichten der Integration

Führen Sie die folgenden Schritte aus, um die Integration zwischen Globaler Bestandsbuchhaltung und Supply Chain Management festzulegen.

1. Melden Sie sich im Supply Chain Management an.
1. Gehen Sie zu **Systemadministration \> Funktion Management**.
1. Wählen Sie **Nach Updates suchen**.
1. Suchen Sie auf der Registerkarte **Alle** nach der Funktion mit dem Namen *(Vorschau) Globale Bestandsbuchhaltung*.
1. Wählen Sie **Jetzt aktivieren**.
1. Gehen Sie zu **Globale Bestandsbuchhaltung \> Einrichten \> Globale Bestandsbuchhaltungsparameter \> Integrationsparameter**.
1. Geben Sie in die Felder **Datendienst-Endpunkt** und **Endpunkt Globale Bestandsbuchhaltung** die URLs aus der E-Mail ein, die das Team der Globalen Bestandsbuchhaltung bei der Anmeldung für die Vorschau gesendet hat.

Die Globale Bestandsbuchhaltung ist nun einsatzbereit.
