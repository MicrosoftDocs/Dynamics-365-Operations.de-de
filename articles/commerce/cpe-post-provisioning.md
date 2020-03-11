---
title: Konfigurieren einer Dynamics 365 Commerce-Vorschauumgebung
description: In diesem Thema wird erläutert, wie eine Microsoft Dynamics 365 Commerce-Vorschauumgebung nach ihrer Bereitstellung konfiguriert wird.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d72caee25c03e8167b94dd387c7861f98bd0f4cb
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057716"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a>Konfigurieren einer Dynamics 365 Commerce-Vorschauumgebung


[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie eine Microsoft Dynamics 365 Commerce-Vorschauumgebung nach ihrer Bereitstellung konfiguriert wird.

## <a name="overview"></a>Übersicht

Führen Sie die in diesem Thema beschriebenen Verfahren erst aus, nachdem Ihre Commerce-Vorschauumgebung bereitgestellt wurde. Informationen zum Bereitstellen Ihrer Commerce-Vorschauumgebung nach deren Bereitstellung finden Sie unter [Stellen Sie eine Commerce-Vorschauumgebung bereit](provisioning-guide.md).

Nachdem Ihre Commerce-Vorschauumgebung vollständig bereitgestellt wurde, müssen zusätzliche Konfigurationsschritte nach der Bereitstellung ausgeführt werden, bevor Sie mit der Evaluierung der Umgebung beginnen können. Um diese Schritte abzuschließen, müssen Sie Microsoft Dynamics Lifecycle Services (LCS) und Dynamics 365 Commerce verwenden.

## <a name="before-you-start"></a>Bevor Sie beginnen

1. Melden Sie sich beim [LCS-Portal](https://lcs.dynamics.com) an.
1. Gehen Sie zu Ihrem Projekt.
1. Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.
1. Wählen Sie Ihre Umgebung in der Liste aus.
1. Wählen Sie in den Umgebungsinformationen rechts die Option **Vollständige Details** aus.
1. Wählen Sie **Anmelden** aus, um ein Menü zu öffnen, und dann **An Umgebung anmelden**.
1. Stellen Sie sicher, dass die juristische Person **USRT** oben rechts ausgewählt ist.

## <a name="configure-the-point-of-sale-in-lcs"></a>Konfigurieren Sie die Verkaufsstelle in LCS

### <a name="associate-a-worker-with-your-identity"></a>Mitarbeiter Ihrer Identität zuordnen

Gehen Sie folgendermaßen vor, um einen Mitarbeiter Ihrer Identität in LCS zuzuordnen.

1. Verwenden Sie das Menü auf der linken Seite, um zu **Module \> Retail und Commerce \> Mitarbeiter \> Arbeitskräfte** zu gehen.
1. Suchen Sie in der Liste den folgenden Datensatz, und wählen Sie ihn aus: **000713 - Andrew Collette**.
1. Wählen Sie im Aktivitätsbereich **Retail** aus.
1. Wählen Sie **Vorhandene Identität zuordnen** aus.
1. Geben Sie im Feld **E-Mail** rechts neben **Suchen mithilfe von E-Mails** Ihre E-Mail-Adresse ein.
1. Wählen Sie **Suchen** aus.
1. Wählen Sie den Datensatz mit Ihrem Namen aus.
1. Wählen Sie **OK**.
1. Wählen Sie **Speichern**.

### <a name="activate-cloud-pos"></a>Aktivieren von Cloud POS

Führen Sie die folgenden Schritte aus, um Cloud POS in LCS zu aktivieren.

1. Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.
1. Wählen Sie Ihre Umgebung in der Liste aus.
1. Wählen Sie in den Umgebungsinformationen rechts die Option **Vollständige Details** aus.
1. Wählen Sie **Anmelden** aus, um ein Menü zu öffnen, und dann **Bei Cloud Point of Sale anmelden**, um die Verkaufsstelle (POS) zu öffnen.
1. Wählen Sie **Weiter**.
1. Melden Sie sich mit Ihrem Microsoft Azure Active Directory-Konto (Azure AD) an.
1. Wählen Sie unter **Shopname** **San Francisco** aus.
1. Wählen Sie **Weiter**.
1. Wählen Sie unter **Register und Gerät** **SANFRAN-1** aus.
1. Wählen Sie **Aktivieren** aus. Sie werden abgemeldet und zur POS-Anmeldeseite weitergeleitet.
1. Sie können sich nun bei der Cloud POS-Erfahrung mit der Operator-ID **000713** und dem Kennwort **123** anmelden.

## <a name="set-up-your-site-in-commerce"></a>Ihre Site in Commerce einrichten

Gehen Sie folgendermaßen vor, um Ihre Vorschau-Site in Commerce einzurichten.

1. Melden Sie sich beim Commerce-Site-Management-Tool mit der URL an, die Sie bei der Initialisierung von E-Commerce während der Bereitstellung notiert haben (siehe [E-Commerce initialisieren](provisioning-guide.md#initialize-e-commerce)).
1. Wählen Sie die Site **Fabrikam** aus, um das Einstellungsdialogfeld der Site zu öffnen.
1. Wählen Sie die Domäne aus, die Sie bei der Initialisierung von E-Commerce eingegeben haben.
1. Wählen Sie als Standardkanal **Erweiterter Fabrikam Online-Store** aus. (Stellen Sie sicher, dass Sie **erweiterter** Online-Store auswählen.)
1. Wählen Sie als Standardsprache **de-de** aus.
1. Lassen Sie das Feld **Pfad** unverändert.
1. Wählen Sie **OK**. Die Liste der Seiten auf der Site wird angezeigt.

## <a name="enable-jobs"></a>Aufträge aktivieren

Um Jobs in Commerce zu ermöglichen, folgen Sie diesen Schritten.

1. Melden Sie sich bei der Umgebung (HQ) an.
1. Verwenden Sie das Menü auf der linken Seite, um zu **Retail and Commerce \> Anfragen und Berichte \> Batch-Jobs** zu gehen.

    Die verbleibenden Schritte dieses Verfahrens müssen für jeden der folgenden Jobs ausgeführt werden:

    * Einzelhandelsauftrag für E-Mail-Benachrichtigung verarbeiten
    * Produktverfügbarkeit
    * P-0001
    * Einzelvorgang für Aufträge synchronisieren

1. Verwenden Sie den Schnellfilter, um nach dem Auftrag anhand seines Namens zu suchen.
1. Wenn der Status des Auftrags **Zurückhalten** lautet, führen Sie die folgenden Schritte aus:

    1. Wählen Sie den Datensatz aus.
    1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Batchauftrag** die Option **Status ändern** aus.
    1. Wählen Sie **Im Wartezustand** und dann **OK** aus.

### <a name="run-full-data-synchronization"></a>Vollständige Datensynchronisation ausführen

Um die vollständige Datensynchronisation im Handel auszuführen, führen Sie die folgenden Schritte aus.

1. Verwenden Sie das Menü auf der linken Seite, um zu **Module \> Retail and Commerce \> Headquarter Einrichtung \> Einzelhandelsplaner \> Kanaldatenbank** zu gehen.
1. In der Liste links wird der Kanal **Standard** ausgewählt. Wählen Sie den anderen verfügbaren Kanal. Dieser Kanal heißt **scXXXXXXXXX**.
1. Wählen Sie **Vollständige Datensynchronisierung** im Aktionsbereich aus.
1. Geben Sie **9999** als Vertriebsplan ein.
1. Wählen Sie **OK**.
1. Wählen Sie **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Testen der Kreditkartendaten, um Testkäufe durchzuführen

Um Testtransaktionen auf der Site durchzuführen, können Sie diese Testkreditkartendaten verwenden:

- **Kartennummer:** 4111-1111-1111-1111
- **Ablaufdatum:** 10/20
- **Kartenprüfwert-Code (CVV):** 737

> [!IMPORTANT]
> Sie sollten unter keinen Umständen versuchen, die tatsächlichen Kreditkarteninformationen auf der Testseite zu verwenden.

## <a name="next-steps"></a>Nächste Schritte

Nachdem die Bereitstellungs- und Konfigurationsschritte abgeschlossen sind, können Sie Ihre Vorschauumgebung bewerten. Verwenden Sie die URL des Commerce-Site-Management-Tools, um zur Autorenerfahrung zu gelangen. Verwenden Sie die URL des Commerce-Site-Management-Tools, um zur Retail-Kundensite-Erfahrung zu gelangen.

Informationen zum Konfigurieren optionaler Funktionen für Ihre Commerce-Vorschauumgebung erhalten Sie unter [Optionale Funktionen für eine Commerce-Vorschauumgebung konfigurieren](cpe-optional-features.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Dynamics 365 Commerce-Vorschauumgebung – Übersicht](cpe-overview.md)

[Bereitstellen einer Dynamics 365 Commerce-Vorschauumgebung](provisioning-guide.md)

[Konfigurieren optionaler Funktionen für eine Dynamics 365 Commerce-Vorschauumgebung](cpe-optional-features.md)

[Dynamics 365 Commerce-Vorschauumgebung – FAQ](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-Portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-Website](https://aka.ms/Dynamics365CommerceWebsite)
