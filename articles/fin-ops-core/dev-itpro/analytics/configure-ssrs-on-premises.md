---
title: SQL Server Reporting Services für lokale Bereitstellungen konfigurieren
description: Dieses Thema liefert Informationen über die Konfiguration von SQL Server Reporting Services (SSRS) für eine lokale Bereitstellung.
author: PeterRFriis
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 3853158afdab545dacda996c984b265eb8947db7f90faf80319841eb01c14910
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726356"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>SQL Server Reporting Services für lokale Bereitstellungen konfigurieren

[!include [banner](../includes/banner.md)]

Gehen Sie nach den Schritten in diesem Thema vor, um SQL Server Reporting Services (SSRS) für Ihre Microsoft Dynamics 365 Finance and Operations (On-Premises)-Bereitstellung zu konfigurieren.

1. Öffnen Sie die Applikation Reporting Services-Konfigurations-Manager.
2. Verwenden Sie den standardmäßigen **Servernamen**, das ist der Name der aktuellen Maschine, und die standardmäßige **Berichtsserverinstanz**, **MSSQLSERVER**.
3. Klicken Sie auf **Verbinden**.

    [![Berichterstellungsdienst-Konfigurationsverbindung.](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. Klicken Sie auf die Registerkarte **Dienstkonto** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.

    [![Registerkarte Dienstkonto.](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. Klicken Sie auf die Registerkarte **Webdienst-URL** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.

    [![Registerkarte Webdienst-URL.](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. Klicken Sie auf die Registerkarte **Datenbank** und stellen Sie sicher, dass die Einstellungen für **Datenbankname** und **Berechtigungseinstellungen** mit der folgenden Graphik übereinstimmen.

    > [!NOTE]
    > Sie müssen eine neue Datenbank erstellen. Dazu klicken Sie auf **Datenbank ändern** und stellen sicher, dass der Name der neuen Datenbank **DynamicsAxReportServer** lautet.

    [![Registerkarte Datenbank.](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. Klicken Sie auf die Registerkarte **Webportal-URL** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.

    > [!NOTE]
    > Sie müssen auf **Übernehmen** klicken, um das Portal ordnungsgemäß zu erstellen und zu konfigurieren.

    [![Registerkarte Webportal-URL.](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    Nachdem das Portal konfiguriert ist, sieht die Registerkarte **Webportal-URL** aus, wie in der folgenden Graphik gezeigt.

    [![Registerkarte Webportal.](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. Klicken Sie auf die Berichts-URL, um das SQL Server Reporting Services-Webportal anzuzeigen.
9. Im Portal erstellen Sie den neuen Ordner **Dynamics**.

    [![Ordner Dynamics.](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. Klicken Sie auf die Registerkarte **Reporting Services-Konfigurations-Manager**, klicken Sie auf die Registerkarte **E-Mail-Einstellungen** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.

    [![Registerkarte E-Mail-Einstellungen.](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. Klicken Sie auf die Registerkarte **Ausführungskonto** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.

    [![Registerkarte Ausführungskonto.](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    Ändern Sie die Standardeinstellungen auf der Registerkarte **Schlüssel** nicht

    [![Registerkarte Schlüssel.](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. Klicken Sie auf die Registerkarte **Abonnementeinstellungen** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.

    [![Registerkarte Abonnementeinstellungen.](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    Ändern Sie die Standardeinstellungen auf der Registerkarte **Bereitstellung für horizontales Skalieren** nicht.

    [![Registerkarte Bereitstellung für horizontales Skalieren.](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    Ändern Sie die Standardeinstellungen auf der Registerkarte **Power BI-Integration** nicht.

    [![Registerkarte Power BI-Integration.](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. Klicken Sie auf **Beenden**, um den **Reporting Services-Konfigurations-Manager** zu schließen.

    [![Reporting Services-Konfigurations-Manager schließen.](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
