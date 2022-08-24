---
title: Eine Dynamics 365 Commerce-Sandbox-Umgebung bereitstellen
description: In diesem Artikel wird erläutert, wie Sie eine Microsoft Dynamics 365 Commerce Sandbox-Umgebung für Demo- oder Sandbox-Nutzung mit integrierten Demodaten bereitstellen.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 1fc50f98055f1df72d255a5be6e863570564b183
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283640"
---
# <a name="provision-a-dynamics-365-commerce-sandbox-environment"></a>Eine Dynamics 365 Commerce-Sandbox-Umgebung bereitstellen

[!include [banner](includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie eine Microsoft Dynamics 365 Commerce Sandbox-Umgebung für Demo-Nutzung mit integrierten Demodaten bereitstellen. Der Prozess zum Einrichten einer Produktionsumgebung ist ähnlich, aber aufwändiger, da viele der Voraussetzungen für die Sandbox-Umgebung bereits in den Demodaten bereitgestellt werden.

Bevor Sie beginnen, empfehlen wir, dass Sie einen kurzen Blick in diesen Artikel werfen, um eine Vorstellung davon zu bekommen, was der Prozess erfordert.

Um eine Commerce-Sandbox-Umgebung erfolgreich bereitzustellen, müssen Sie einige Parameter für die Umgebung und die Commerce Scale Unit (CSU) angeben, die verwendet werden, wenn Sie Commerce später bereitstellen. In den Anweisungen in diesem Artikel werden alle Schritte, die zum Ausführen der Bereitstellung erforderlich sind, sowie die Parameter, die Sie verwenden müssen, beschrieben.

Nach der erfolgreichen Bereitstellung Ihrer Commerce-Umgebung müssen Sie einige Schritte nach der Bereitstellung ausführen, um Ihre Vorschauumgebung vorzubereiten. Einige Schritte sind optional, je nachdem, welche Aspekte des Systems Sie verwenden möchten. Sie können die optionalen Schritte später jederzeit ausführen.

Informationen zum Konfigurieren Ihrer Commerce-Umgebung nach deren Bereitstellung finden Sie unter [Konfigurieren Sie eine Commerce-Umgebung](cpe-post-provisioning.md). Informationen zum Konfigurieren optionaler Funktionen für Ihre Commerce-Umgebung erhalten Sie unter [Optionale Funktionen für eine Commerce-Sandbox-Umgebung konfigurieren](cpe-optional-features.md).

## <a name="prerequisites"></a>Voraussetzungen

Die folgenden Voraussetzungen müssen erfüllt sein, damit Sie Ihre Commerce-Umgebung bereitstellen können:

- Sie haben Zugriff auf das Microsoft Dynamics Lifecycle Services-Portal (LCS).
- Sie sind ein vorhandener Microsoft Dynamics 365-Partner oder -Kunde und verfügen über ein Implementierungsprojekt, das bereits erstellt wurde und in LCS verwendet werden kann.  
- Sie haben eine Azure Active Directory (Azure AD)-Sicherheitsgruppe erstellt, die als eine E-Commerce-Systemadministrator-Gruppe verwendet wird, und Ihnen liegt deren ID vor.
- Sie haben eine Azure AD-Sicherheitsgruppe erstellt, die als Bewertungs- und Prüfungsmoderatorgruppe verwendet wird, und Ihnen liegt deren ID vor. (Diese Sicherheitsgruppe kann mit der Administratorgruppe des Commerce-Systems identisch sein.)
- Sie haben eine Zentralverwaltungsinstanz in LCS bereitgestellt. Weitere Informationen finden Sie unter [Einrichten einer neuen Umgebung](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).

Beachten Sie, dass diese Liste nicht vollständig ist. Sollten Probleme auftreten, wenden Sie sich an Ihren Microsoft-Partner, um Unterstützung zu erhalten.

## <a name="provision-your-commerce-environment"></a>Bereitstellen Ihrer Commerce-Umgebung

Im folgenden Verfahren wird erläutert, wie eine Commerce-Umgebung bereitgestellt wird. Nachdem Sie die Schritte erfolgreich abgeschlossen haben, kann Ihre Commerce-Umgebung konfiguriert werden. Alle unten beschriebenen Schritte finden im LCS-Portal statt.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Initialisieren der Commerce Scale Unit (Cloud)

Führen Sie folgende Schritte aus, um die CSU zu initialisieren.

1. Wählen Sie in LCS Ihre Umgebung aus der Liste aus.
1. Wählen Sie in der **UMGEBUNGEN**-Ansicht rechts die Option **Vollständige Details** aus. Die Ansicht zu Umgebungsdetails wird angezeigt.
1. Wählen Sie im Abschnitt **Umgebung verwalten** unter **UMGEBUNGSFUNKTIONEN** die Option **Verwalten** aus.
1. Wählen Sie auf der Registerkarte **Commerce Scale Units** die Option **Initialisieren** aus. Die Ansicht **Skalierungseinheit hinzufügen** erscheint.
1. Wählen Sie im Feld **REGION** die Region aus, die mit der Region identisch ist, in der Sie die Umgebung bereitgestellt haben.
1. Wählen Sie in der Dropdown-Liste **Version** die neueste verfügbare Version aus.
1. Wählen Sie **Initialisieren** aus.
1. Wählen Sie im Warndialogfeld, in dem Sie aufgefordert werden, die Initialisierung der Commerce Scale Unit zu bestätigen **Ja** aus. Die CSU wurde jetzt für die Bereitstellung in die Warteschlange gestellt.
1. Stellen Sie vor dem Fortfahren sicher, dass Ihr CSU-Status **ERFOLGREICH** lautet. Die Initialisierung dauert ungefähr zwei bis fünf Stunden.

Wenn Sie den Link **Verwalten** in der Ansicht „Umgebungsdetails“ nicht finden können, wenden Sie sich an Ihren Microsoft-Kontakt, um Unterstützung zu erhalten.

### <a name="initialize-e-commerce"></a>E-Commerce initialisieren

Führen Sie folgende Schritte aus, um Commerce zu initialisieren.

1. Auf der Registerkarte **E-Commerce** wählen Sie **Einstellungen** aus.
1. Geben Sie im Feld **E-Commerce-Evaluierungsname** einen Namen ein. Beachten Sie, dass dieser Name in einigen URLs sichtbar ist, die auf Ihre E-Commerce-Instanz verweisen.
1. Wählen Sie im Feld **Commerce Scale Unit Name** Ihre CSU in der Liste aus. (Die Liste sollte nur eine Option haben.)

    Das Feld **E-Commerce-Geografie** wird automatisch eingestellt.

1. Wählen Sie **Weiter** aus, um fortzufahren.
1. Geben Sie im Feld **Unterstützte Hostnamen** eine gültige Domäne, wie `www.fabrikam.com`, ein.
1. Geben Sie in das Feld **AAD-Sicherheitsgruppe für Systemadministrator** die ersten Buchstaben des Namens der Sicherheitsgruppe ein, die Sie verwenden möchten, und wählen Sie dann das Lupensymbol aus, um die Suchergebnisse anzuzeigen. Wählen Sie die richtige Sicherheitsgruppe in der Liste aus.
1.  Geben Sie in das Feld **AAD-Sicherheitsgruppe für Bewertungs- und Prüfungsmoderator** die ersten Buchstaben des Namens der Sicherheitsgruppe ein, die Sie verwenden möchten, und wählen Sie dann das Lupensymbol aus, um die Suchergebnisse anzuzeigen. Wählen Sie die richtige Sicherheitsgruppe in der Liste aus.
1. Lassen Sie die Option **Bewertungs- und Prüfungsdienst aktivieren** auf **Ja** festgelegt.
1. Wählen Sie **Initialisieren** aus. In der Ansicht **Commerce-Verwaltung** wird erneut angezeigt, wo die Registerkarte **E-Commerce** ausgewählt ist. Die E-Commerce-Initialisierung wurde gestartet.
1. Warten Sie, bevor Sie fortfahren, bis Ihr E-Commerce-Initialisierungsstatus **INITIALISIERUNG ERFOLGREICH** lautet.
1. Notieren Sie sich unten rechts im Bereich **Links** die URLs für die folgenden Links:

    * **E-Commerce-Website** – Der Link zum Stammverzeichnis Ihrer E-Commerce-Website.
    * **Commerce-Site-Builder** – Der Link zum Site-Management-Tool.

## <a name="next-steps"></a>Nächste Schritte

Um den Prozess zum Bereitstellen und Konfigurieren Ihrer Commerce-Umgebung fortzusetzen, schauen Sie sich [Konfigurieren Sie eine Commerce-Sandbox-Umgebung](cpe-post-provisioning.md) an.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eine Dynamics 365 Commerce-Sandbox-Umgebung konfigurieren](cpe-post-provisioning.md)

[BOPIS in einer Dynamics 365 Commerce-Sandbox-Umgebung konfigurieren](cpe-bopis.md)

[Optionale Funktionen für eine Dynamics 365 Commerce-Sandbox-Umgebung konfigurieren](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (Cloud)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-Portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-Website](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
