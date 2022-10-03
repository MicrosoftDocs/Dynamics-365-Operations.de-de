---
title: Konfiguration für Finance Insights
description: In diesem Artikel werden die Konfigurationsschritte erläutert, mit denen Ihr System die in Finance Insights verfügbaren Funktionen nutzen kann.
author: ShivamPandey-msft
ms.date: 09/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 05bf5fe5a5ff86bbf52ed58ee6b1e84c15bf2c1e
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573193"
---
# <a name="configuration-for-finance-insights"></a>Konfiguration für Finance Insights

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights kombiniert Funktionen von Microsoft Dynamics 365 Finance mit Dataverse, Azure und AI Builder, um leistungsstarke Prognosetools für Ihr Unternehmen zu bieten. In diesem Artikel werden die Konfigurationsschritte erläutert, mit denen Ihr System die in Finance Insights verfügbaren Funktionen nutzen kann. Um die Verfahren in diesem Artikel erfolgreich abzuschließen, müssen Sie über Systemadministrator- und Systemanpasserzugriff im [Power Portal Admin Center](https://admin.powerplatform.microsoft.com/), Systemadministratorzugriff in Dynamics 365 Finance und über Zugriff zum Erstellen von Umgebungen in Microsoft Dynamics Lifecycle Services (LCS) verfügen.

> [!NOTE]
> Die folgenden Prozeduren zum Einrichten von Finance Insights gelten für die Versionen von Dynamics 365 Finance 10.0.21 oder höher.

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 Finance bereitstellen

Gehen Sie folgendermaßen vor, um die Umgebungen bereitzustellen.

1. Im LCS erstellen oder aktualisieren Sie eine Dynamics 365 Finance-Umgebung. Die Umgebung erfordert App-Version 10.0.21 oder höher.

    > [!NOTE]
    > Die Umgebung muss eine Hochverfügbarkeitsumgebung (HA-Umgebung) sein. (Diese Art von Umgebung wird auch als Ebene-2-Umgebung bezeichnet.) Weitere Informationen finden Sie unter [Umgebungsplanung](/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

2. Wenn Sie Finance Insights in einer Sandbox-Umgebung konfigurieren, müssen Sie möglicherweise Produktionsdaten erst in diese Umgebung kopieren, damit Vorhersagen funktionieren. Das Vorhersagemodell verwendet Daten aus mehreren Jahren, um Vorhersagen zu erstellen. Die Contoso-Demodaten enthalten nicht genügend historische Daten, um das Vorhersagemodell angemessen zu trainieren. 

## <a name="configure-your-azure-ad-tenant"></a>Azure AD-Mandanten-ID konfigurieren

Azure Active Directory (Azure AD) muss so konfiguriert werden, dass es mit Dataverse und den Microsoft Power Platform-Anwendungen verwendet werden kann. Diese Konfiguration erfordert, dass entweder die **Projektbesitzer**-Rolle oder die **Umgebungsmanager**-Rolle dem Benutzer im **Projektsicherheitsrolle**-Feld in LCS zugewiesen werden.

Stellen Sie sicher, dass die folgende Einrichtung abgeschlossen ist:

- Sie haben **Systemadministrator** und **Systemanpasser**-Zugriff im Power Portal Admin Center.
- Eine Dynamics 365 Finance- oder eine gleichwertige Lizenz wird auf den Benutzer angewendet, der das Finance Insights-Add-In installiert.
- Folgende Azure AD-Apps sind in Azure AD registriert.

    |  Anwendung                             | App-Kennung                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP-Microservices-CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |

    Um zu überprüfen, ob die Anwendung in Azure AD registriert ist, prüfen Sie die Liste **Alle Anwendungen**. Weitere Einzelheiten finden Sie unter [Unternehmensanwendungen anzeigen](/azure/active-directory/manage-apps/view-applications-portal).
  
    Wenn die Anwendung nicht in Azure AD registriert ist, wenden Sie sich an den Support.
  
## <a name="configure-dataverse"></a>Dataverse konfigurieren

Gehen Sie folgendernamßen vor, um Dataverse für Finance Insights zu konfigurieren.

- Öffnen Sie die Seite „Umgebung“ in LCS und überprüfen Sie, ob der Abschnitt **Power Platform-Integration** bereits eingerichtet ist.

    - Wenn Dataverse bereits eingerichtet ist, sollte der Name der Dataverse-Umgebung, die mit der Finance-Umgebung verknüpft ist, aufgelistet sein.
    - Wenn Dataverse noch nicht eingerichtet ist, wählen Sie **Setup**. Die Einrichtung der Dataverse-Umgebung kann bis zu einer Stunde dauern. Wenn das Setup erfolgreich abgeschlossen wird, sollte der Name der Dataverse-Umgebung, die mit der Finance-Umgebung verknüpft ist, aufgelistet werden.
    - Wenn diese Integration mit einer bestehenden Microsoft Power Platform-Umgebung eingerichtet wurde, wenden Sie sich an Ihren Administrator, um sicherzustellen, dass die verknüpfte Umgebung nicht deaktiviert ist.

        Weitere Informationen finden Sie unter [Aktivieren der Power Platform-Integration](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Um auf die Microsoft Power Platform-Admin-Site zuzugreifen, gehen Sie zu <https://admin.powerplatform.microsoft.com/environments>.

## <a name="configure-the-finance-insights-add-in"></a>Finance Insights Add-in konfigurieren

Wenn Sie das Finance Insights-Add-In bereits installiert haben, deinstallieren Sie es, bevor Sie das folgende Verfahren ausführen.

> [!NOTE]
> Wenn Sie das Data Lake-Add-In bereits in LCS installiert haben, verwendet Finance Insights es, um Daten zu speichern, die für Vorhersagen erforderlich sind. Wenn Sie das Data Lake-Add-In noch nicht in LCS installiert haben, erstellt das Finance Insights-Add-In einen verwalteten Data Lake für Sie.

Führen Sie diese Schritte aus, um das Finance Insights-Add-In zu installieren.

1. Melden Sie sich bei LCS an und wählen Sie dann unter dem Umgebungsnamen auf der rechten Seite der Seite **Alle Einzelheiten** aus.
2. Wählen Sie Im Abschnitt **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.
3. Wählen Sie das **Finance insights**-Add-In aus.
4. Stimmen Sie den allgemeinen Geschäftsbedingungen zu und wählen Sie dann **Installieren** aus.

Die Installation des Add-Ins kann einige Minuten dauern.

## <a name="one-last-thing"></a>Noch eine Sache ...

Nach erfolgreicher Installation des Add-Ins kann es bis zu einer Stunde dauern, bis Sie Finance Insights-Funktionen im Arbeitsbereich **Funktionsverwaltung** in Dynamics 365 Finance aktivieren können. Wenn Sie nicht so lange warten möchten, können Sie den Prozess **Insights-Bereitstellungsstatus überprüfen** manuell ausführen. 

1. Gehen Sie in Dynamics 365 Finance zu **Systemverwaltung \> Einrichten \> Prozessautomatisierung**.
2. Suchen Sie in der Registerkarte **Hintergrundprozesse** **Insights-Bereitstellungsstatus überprüfen** und wählen Sie **Bearbeiten** aus.
3. Setzen Sie das Feld **Nächste Ausführung** auf 30 Minuten vor der aktuellen Uhrzeit.

   Diese Änderung sollte den Prozess **Insights-Bereitstellungsstatus überprüfen** sofort ausgeführt werden.

   Nachdem der Prozess **Insights-Bereitstellungsstatus überprüfen** erfolgreich ausgeführt wurde, können Sie die Funktionen von Finance Insights im Arbeitsbereich **Funktionsverwaltung** aktivieren.

> [!NOTE]
> Wenn der Prozess **Insights Bereitstellungsstatusprüfung** nicht ausgeführt wird, gehen Sie zu **Systemverwaltung** > **Abfragen** > **Batchaufträge**. Ändern Sie im Feld **Automatisierungsabrufsystem verarbeiten** den Wert auf **Warten**, um den Prozess zu starten. 
> 
## <a name="feedback-and-support"></a>Feedback und Support

Wenn Sie an Feedback interessiert sind oder Support brauchen, senden Sie eine E-Mail an [Finance insights (Vorschau)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
