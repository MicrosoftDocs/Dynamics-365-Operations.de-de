---
title: Talent mit Power Apps und Power Automate erweitern
description: Dieser Artikel beschreibt einige Beispiele für Erweiterungsszenarien für Microsoft Dynamics 365 Human Resources, die Microsoft Power Apps und Microsoft Power Automate verwenden.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5b1ebe17063d954b52a0607d39e3ea08518adb89
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057597"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Mit Power Apps und Power Automate erweitern

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieser Artikel beschreibt einige Beispiele für Erweiterungsszenarien für Microsoft Dynamics 365 Human Resources, die Microsoft Power Apps und Microsoft Power Automate verwenden. Sie können das Lösungspaket importieren, das jedem Beispiel in der Power Apps-Umgebung zugeordnet ist. Sie können entweder die Pakete als Anleitung oder als Startpunkte zu den Werkzeugszenarien verwenden, die der Organisation zugeordnet sind.

> [!IMPORTANT]
> Wenn Sie die Vorlagen und Apps verwenden möchten, die in diesem Thema als „wie vorliegend“ beschrieben sind, müssen Sie diese unbedingt testen, um sicherzustellen, dass sie alle Szenarien beinhalten, die für Ihre Implementierung bestimmt sind.

## <a name="prerequisites"></a>Voraussetzungen

- Um Pakete zu importieren, müssen Benutzer die Berechtigung **Umgebungs-Hersteller** haben.
- Um Apps zu exportierenden oder zu importieren, müssen Benutzer eine Lizenz für Power Apps Plan 2 oder eine Testlizenz für Power Apps-Plan 2 haben.

## <a name="integration-with-microsoft-365-power-automate"></a>Integration in Microsoft 365, Power Automate

Die **Integration in Microsoft 365**-App kann verwendet werden, um Teaminformationen für angemeldete Benutzer von Microsoft 365 zu extrahieren. Es verweist auf Arbeitskräfte in Human Resources, um Mitarbeiteridentifikationstypen zu extrahieren. Manager können das Ablaufdatum von Mitarbeiter-ID-Typen überprüfen. Sie können auch eine E-Mail-Erinnerung senden, wenn der Typ der Mitarbeiter-ID abläuft. Power Automate kann in Power Apps integriert werden, um diese Erinnerung zu senden. Power Apps erhält eine Bestätigung von Power Automate, wenn die Erinnerung gesendet wird. Zu den Identifikationstypen gehören Führerschein, Reisepass und andere zulässige Ausweispapiere.

Sie können diese App für andere Szenarien erweitern. Sie können sie zum Beispiel verwenden, um Teamferieninformationen, Kalenderereignisse und weitere teamspezifische Ereignisse anzuzeigen.

Um die App **Integration in Microsoft 365, Power Automate**-App herunterzuladen, wechseln Sie zu [Integration in Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) im Microsoft Download Center.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate - SQL Verbinden und ausführen

Die Vorlage **Power Automate - SQL Connect and execute** verbindet sich mit Microsoft SQL Server und ermöglicht die Ausführung von SQL-Abfragen.

Obwohl diese Vorlage SQL-Tabellen liest und aktualisiert, können Sie sie erweitern und für andere Szenarien verwenden. Sie können sie beispielsweise verwenden, um eine Stagingtabelle in Dataverse mit Datensätzen von SQL Server zu füllen und um die Stagingtabelle regelmäßig zu synchronisieren, indem ein inkrementeller Push von SQL Server verwendet wird.

Die erweiterte Abfrage ist in Flow integriert, um die Datentransformation und die inkrementelle Übertragung zu ermöglichen.

Um die **Power Automate - SQL Connect and execute** Vorlage herunterzuladen, gehen Sie zu [Power Automate - SQL Connect und führen Sie](https://go.microsoft.com/fwlink/?linkid=2081789) im Microsoft Download Center aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Das Microsoft Power Platform](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]