---
title: "SQL Server Reporting Services für eine lokale Bereitstellung konfigurieren"
description: "Dieses Thema liefert Informationen über die Konfiguration von SQL Server Reporting Services (SSRS) für eine lokale Bereitstellung."
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 2ecfb759a59292ddbce484b3ae20368c486fedd9
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a>SQL Server Reporting Services für eine lokale Bereitstellung konfigurieren

[!include [banner](../includes/banner.md)]

Gehen Sie nach den Schritten in diesem Thema vor, um SQL Server Reporting Services (SSRS) für ihre Bereitstellung von Microsoft Dynamics 365 for Finance and Operations (On-Premises) zu konfigurieren.

1. Öffnen Sie die Applikation Reporting Services-Konfigurations-Manager.
2. Verwenden Sie den standardmäßigen **Servernamen**, das ist der Name der aktuellen Maschine, und die standardmäßige **Berichtsserverinstanz**, **MSSQLSERVER**. 
3. Klicken Sie auf **Verbinden**.
   
   [![Reporting Services-Konfigurationsverbindung](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)
   
4. Klicken Sie auf die Registerkarte **Dienstkonto** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.

    [![Registerkarte Dienstkonto](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)
    
5. Klicken Sie auf die Registerkarte **Webdienst-URL** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen. 

    [![Registerkarte Webdienst-URL](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png) 
    
6. Klicken Sie auf die Registerkarte **Datenbank** und stellen Sie sicher, dass die Einstellungen für **Datenbankname** und **Berechtigungseinstellungen** mit der folgenden Graphik übereinstimmen. **Hinweis:** Sie müssen eine neue Datenbank erstellen. Dazu klicken Sie auf **Datenbank ändern** und stellen sicher, dass der Name der neuen Datenbank **DynamicsAxReportServer** lautet.

    [![Registerkarte Datenbank](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)
    
7. Klicken Sie auf die Registerkarte **Webportal-URL** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen. **Hinweis:** Sie müssen auf **Übernehmen** klicken, um das Portal ordnungsgemäß zu erstellen und zu konfigurieren.

    [![Registerkarte Webportal-URL](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)
    
   Nachdem das Portal konfiguriert ist, sieht die Registerkarte **Webportal-URL** aus, wie in der folgenden Graphik gezeigt.
    [![Registerkarte Webportal](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)
    
8. Klicken Sie auf die Berichts-URL, um das SQL Server Reporting Services-Webportal anzuzeigen. 
9. Im Portal erstellen Sie den neuen Ordner **Dynamics**.

   [![Ordner Dynamics](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)
    
10. Klicken Sie auf die Registerkarte **Reporting Services-Konfigurations-Manager**, klicken Sie auf die Registerkarte **E-Mail-Einstellungen** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.

    [![Registerkarte E-Mail-Einstellungen](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)
    
11. Klicken Sie auf die Registerkarte **Ausführungskonto** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.

    [![Registerkarte Ausführungskonto](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)
    
    Ändern Sie die Standardeinstellungen auf der Registerkarte **Verschlüsselungs-Schlüssel** nicht. [![Registerkarte Verschlüsselungs-Schlüssel](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)
    
12. Klicken Sie auf die Registerkarte **Abonnementeinstellungen** und stellen Sie sicher, dass die Einstellungen mit der folgenden Graphik übereinstimmen.

    [![Registerkarte Abonnementeinstellungen](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)
    
    Ändern Sie die Standardeinstellungen auf der Registerkarte **Bereitstellung für horizontales Skalieren** nicht. [![Registerkarte Bereitstellung für horizontales Skalieren](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)
    
    Ändern Sie die Standardeinstellungen auf der Registerkarte **Power BI-Integration** nicht. [![Registerkarte Power BI Integration](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png) 
    
13. Klicken Sie auf **Beenden**, um den **Reporting Services-Konfigurations-Manager** zu schließen.

    [![Reporting Services-Konfigurations-Manager schließen](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)
    


