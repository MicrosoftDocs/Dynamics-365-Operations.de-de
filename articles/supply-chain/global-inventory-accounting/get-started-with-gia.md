---
title: Einstieg in die Globale Bestandsbuchhaltung
description: In diesem Artikel wird beschrieben, wie Sie mit der Globalen Bestandsbuchhaltung loslegen.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cbe6bff6fab96900b8bd4e112a8858363fff86d1
ms.sourcegitcommit: 9870b773a2ea8f5675651199fdbc63ca7a1b4453
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013554"
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

## <a name="how-to-get-the-global-inventory-accounting-add-in"></a><a name="sign-up"></a>Wie Sie das Add-In der Globalen Bestandsbuchhaltung erhalten

> [!IMPORTANT]
> Um die Globale Bestandsbuchhaltung zu verwenden, müssen Sie über eine LCS-fähige Hochverfügbarkeitsumgebung verfügen (keine OneBox-Umgebung). Außerdem müssen Sie Supply Chain Management Version 10.0.19 oder höher ausführen.

### <a name="supply-chain-management-version-10019-to-10026"></a>Supply Chain Management Version 10.0.19 bis 10.0.26

Um Global Inventory Accounting for Supply Chain Management Version 10.0.19 bis 10.0.26 zu installieren, beginnen Sie mit [Add-In installieren](#install). Senden Sie dann Ihre LCS-Umgebungs-ID und Ihren Firmennamen per E-Mail an das [Globale Bestandsbuchhaltungsteam](mailto:GlobalInvAccount@microsoft.com). Ihnen sendet das Team eine Nachverfolgungs-E-Mail, die Ihre Globale Bestandsbuchhaltung Service-Endpunkte enthält.

### <a name="supply-chain-management-version-10027-and-later"></a>Supply Chain Management Version 10.0.27 und höher

Um Global Inventory Accounting for Supply Chain Management Version 10.0.27 und höher führen Sie einfach [Add-In installieren](#install) aus. Für diese Versionen von Supply Chain Management werden die Endpunkte des Global Inventory Accounting Service automatisch eingerichtet, sodass Sie sie nicht manuell suchen müssen. Wenn beim Einrichten des Add-Ins Probleme auftreten, wenden Sie sich bitte an die [Globales Bestandsbuchhaltungsteam](mailto:GlobalInvAccount@microsoft.com).

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

## <a name="install-the-add-in"></a><a name="install"></a>Installieren des Add-Ins

Gehen Sie folgendermaßen vor, um das Add-In zu installieren, damit Sie die Globale Bestandsbuchhaltung verwenden können.

1. Melden Sie sich bei [LCS](https://lcs.dynamics.com/Logon/Index) an.
1. Öffnen Sie die LCS-Umgebung, in der Sie den Dienst hinzufügen möchten.
1. Gehen Sie zu **Vollständige Details**.
1. Gehen Sie zu **Power Platform Integration**, und wählen Sie **Einrichten**.
1. Aktivieren Sie im Dialogfeld **Einrichten der Power Platform Umgebung** das Kontrollkästchen und wählen Sie dann **Einrichten**. In der Regel dauert das Einrichten zwischen 60 und 90 Minuten.
1. Nachdem die Einrichtung der Microsoft Power Platform-Umgebung abgeschlossen ist, melden Sie sich beim [Power Platform-Admin Center](https://admin.powerplatform.microsoft.com) an, und installieren Sie das Global Inventory Accounting-Add-In, indem Sie die folgenden Schritte ausführen:
   1. Wählen Sie die Umgebung, in der Sie das Add-In installieren möchten.
   1. Wählen Sie **Dynamics 365-Apps**
   1. Wählen Sie **App installieren**.
   1. Wählen Sie **Dynamics 365 Global Inventory Accounting**.
   1. Wählen Sie zum Installieren **Weiter** aus.
1. Zurück zur LCS-Umgebung. Wählen Sie auf dem Inforegister **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.
1. Wählen Sie **Globale Bestandsbuchhaltung**.
1. Befolgen Sie die Installationsanleitung und erklären Sie sich mit den Allgemeinen Geschäftsbedingungen einverstanden.
1. Wählen Sie **Installieren**.
1. Auf der Registerkarte **Umgebungs-Add-Ins** Inforegister sollten Sie sehen, dass Globale Bestandsbuchhaltung installiert wird. Nach einigen Minuten sollte sich der Status von *Installieren* in *Installiert* ändern. (Möglicherweise müssen Sie die Seite aktualisieren, um diese Änderung zu sehen.) An diesem Punkt ist die Globale Bestandsbuchhaltung einsatzbereit.

Wenn die Standardsprache Ihrer Dataverse-Installation nicht Englisch ist, gehen Sie wie folgt vor:
1. Gehen Sie zu **Erweiterte Einstellung \> Verwaltung \> Sprachen**.
1. Wählen Sie *Englisch* (*LanguageCode=1033*), und wählen Sie dann **Anwenden**.

## <a name="set-up-the-integration"></a>Einrichten der Integration

Führen Sie die folgenden Schritte aus, um die Integration zwischen Globaler Bestandsbuchhaltung und Supply Chain Management festzulegen.

1. Melden Sie sich im Supply Chain Management an.
1. Gehen Sie zu **Systemadministration \> Funktion Management**.
1. Wählen Sie **Nach Updates suchen**.
1. Suchen Sie auf der Registerkarte **Alle** nach der Funktion mit dem Namen *(Vorschau) Globale Bestandsbuchhaltung*.
1. Wählen Sie **Jetzt aktivieren**.
1. Gehen Sie zu **Globale Bestandsbuchhaltung \> Einrichten \> Globale Bestandsbuchhaltungsparameter \> Integrationsparameter**.
1. Führen Sie je nach Art der Version von Supply Chain Management einen der folgenden Schritte aus:
    - **Supply Chain Management-Version 10.0.19 auf 10.0.26**: In dem **Endpunkt des Datendienstes** und **Endpunkt der globalen Bestandsbuchhaltung** geben Sie in die Felder die URLs ein, die Ihnen per E-Mail vom Team Global Inventory Accounting zugesandt wurden (siehe auch [So erhalten Sie das Global Inventory Accounting-Add-In](#sign-up)).
    - **Supply Chain Management Version 10.0.27 und neuer**: Sie müssen die Endpunkte nicht eingeben, daher können Sie diesen Schritt überspringen.

Die Globale Bestandsbuchhaltung ist nun einsatzbereit.
