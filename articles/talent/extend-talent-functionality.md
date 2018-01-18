---
title: "Erweitern Sie die Funktionalität von Microsoft Dynamics 365 for Talent"
description: "Wenn Sie Microsoft PowerApps erstellt haben, können Sie diese Anwendungen von Links innerhalb von Microsoft Dynamics 365 for Talent starten."
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Talent
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cfd3b475b113fdab4ceeb3e636fea6c9134ab982
ms.openlocfilehash: 0ab829803634871c9060daa381bd02d7d2bbdf42
ms.contentlocale: de-de
ms.lasthandoff: 12/01/2017

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a>Erweitern Sie die Funktionalität von Microsoft Dynamics 365 for Talent
Wenn Sie Microsoft PowerApps erstellt haben, können Sie diese Anwendungen von Links innerhalb von Microsoft Dynamics 365 for Talent starten. Um Zugriff auf Ihre Bewerbungen einzurichten, müssen Sie einige Informationen im Talent auf einer Konfigurationsseite eirichten die Sie aus dem Arbeitsbereich **Systemverwaltung** öffnen können.

## <a name="configuring-embedded-powerapps-within-talent"></a>Konfigurieren von eingebetteten PowerApps innerhalb von Talent
Verwenden Sie die Seite **Satz eingebettetes Microsoft PowerApps**, um Talent Seiten zu konfigurieren, um PowerApps-Bewerbungen zu starten. Um die Seite **Legen Sie eingebettetes Microsoft PowerApps fest** zu öffnen, öffnen Sie die Verknüpfung **Systemverwaltung** und anschließend **Links** auswählen Registerkarte **Microsoft PowerApps** in der Gruppe **Einstellungen**. 

Die folgenden Informationen werden auf dieser Seite eingegeben oder festgelegt: 

> - Ein beschreibender Name oder eine Kennung für die PowerApps-Bewerbung.
> - Eine eindeutige Kennung (GUID) für jede Anwendung, die Sie einer Talent Seite hinzufügen. Anwendungs-ID ist im Feld PowerApps-Standort, [powerapps.com](http://powerapps.com/) verfügbar. 
> - Die Seite, von der Benutzer eine Anwendung oder öffnen kann Nicht alle Talent Seiten unterstützen eingebettete PowerApps und Power BI-Berichte. 

 > [!NOTE]
 >  Geben Sie hier den internen Namen der Seite ein, anstatt den Anzeigenamen, der am oberen Seitenrand erscheint. Um den internen Namen zu suchen, öffnen Sie die Seite für den internen Namen und klicken Sie irgendwo auf der Seite mit der rechten Maustaste. Wenn das Menü sich öffnet, zeigen Sie im **Formularinformationen** auf Artikel. Der interne Formularname wird neben dem Menü **Formularinformationen** angezeigt.
 
> - Definieren Sie das Formularsteuerelement, aus dem die Bewerbung Kontextdaten erwerben kann. So kann beispielsweise eine Anwendung Daten zu einer Arbeitskraft nutzen. Wenn Sie die Seite **Arbeitskraft** im Feld **Kontext** eingeben, wird die Seite **Arbeitskraft** geöffnet, wenn Sie die Bewerbung starten. Ein Eintrag ist im **Kontextfeld** optional. 
> - Legen Sie die Größe des Dialogfelds fest, an dem die PowerApps-Bewerbung ausgeführt wird. Die Dialogfelder werden als "klein"oder "groß" festgelegt, um die Benutzeroberfläche zu optimieren, wenn Sie Ihre Bewerbung auf einem Telefon oder einem größeren Gerät laufen lassen. 

Sie können auch angeben, für welche juristische Personen eine Bewerbung verfügbar ist, oder Sie können Produktbeziehungen Katalogs für alle juristischen Personen vefügbar machen. Standardmäßig sind die PowerApps-Bewerbungen für alle juristischen Personen verfügbar.

## <a name="opening-an-application"></a>Öffnen Sie eine Bewerbung
Wenn Sie eingebettete PowerApps-Bewerbungen konfigurieren, werden Links für Anwendungen, die Sie zuvor definiert haben, zu Seiten innerhalb von Talent hinzugefügt. Klicken Sie auf einen Link, um eine Bewerbung zu öffnen. 



