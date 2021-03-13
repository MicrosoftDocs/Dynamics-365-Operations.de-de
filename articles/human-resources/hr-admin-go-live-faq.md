---
title: FAQ live schalten
description: In diesem Thema werden häufig gestellte Fragen zur Liveschaltung mit einem Dynamics 365 Human Resources Implementierungsprojekt behandelt.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5041d515b261bb3e4b14885e0ec0ce788edf729
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112651"
---
# <a name="go-live-faq"></a>FAQ live schalten 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden häufig gestellte Fragen zur Liveschaltung mit einem Dynamics 365 Human Resources Implementierungsprojekt behandelt. 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>Wann kann ich meine Produktionsumgebung konfigurieren und anfordern? 

In der Regel wird eine Produktionsumgebung bereitgestellt, nachdem die folgenden Kriterien erfüllt wurden:

- Alle Anpassungen sind vollständig.
- Der User Acceptance Test (UAT) ist abgeschlossen.
- Der Kunde hat die Lösung abgemeldet.
- Es gibt keine Blockierungsprobleme für die Inbetriebnahme. 

Wenn sich qualifizierte Kunden in dieser Phase befinden, arbeitet das Microsoft FastTrack-Team mit dem Projektteam zusammen, um eine Go-Live-Bewertung durchzuführen. 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>Was sind die Voraussetzungen für die Bereitstellung einer Produktionsumgebung? 

Eine Liste der Voraussetzungen finden Sie unter [Bereiten Sie sich auf die Inbetriebnahme vor](hr-admin-go-live-prepare.md). 

## <a name="what-is-a-go-live-assessment"></a>Was ist eine Go-Live-Bewertung?  

Die Go-Live-Bewertung ist Teil des [Microsoft FastTrack-Programms](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). Während dieser Überprüfung bewertet ein Lösungsarchitekt, ob ein Implementierungsprojekt für eine erfolgreiche Umstellung und Inbetriebnahme bereit ist. Diese Überprüfung ist für jedes Implementierungsprojekt obligatorisch, bevor Sie die Inbetriebnahme in einer Produktionsumgebung anfordern können. 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>Unsere Sandbox-Umgebungen werden im zentralen US-Rechenzentrum bereitgestellt. Wir möchten, dass unsere Produktionsumgebungen im Rechenzentrum im Westen der USA bereitgestellt werden. Kann ich in meiner Produktionskonfiguration West US als Rechenzentrum auswählen? 

LCS hindert Sie nicht daran, ein anderes Rechenzentrum auszuwählen, wenn Sie eine Personalumgebung bereitstellen. Wir empfehlen jedoch dringend, kein anderes Rechenzentrum auszuwählen.  

Wenn Sie möchten, dass sich Ihre Produktionsumgebung im Rechenzentrum in den USA befindet, sollten Sie zuerst Ihre Sandbox-Umgebungen im Rechenzentrum in den USA erneut bereitstellen, testen und abmelden. 

Informationen zur Auswahl des richtigen Rechenzentrums finden Sie unter [Netzwerkanforderungen](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements). 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>Welche Zugriffsebene habe ich für meine Personalumgebungen auf die Azure-Ressourcen?  

Der Zugriff auf die Personalumgebungen ist begrenzt. Sie können nicht auf die virtuelle Maschine (VM) oder Microsoft Internet Information Services (IIS) zugreifen. Sie können auch nicht über auf die Datenbank über Microsoft SQL Server Management Studio zugreifen. 

Sie können zwar nicht auf Ihre Azure-Ressourcen Dynamics 365 Human Resources Umgebungen direkt zugreifen, aber es gibt es zusätzliche Funktionen, mit denen Sie auf Ihre Daten zugreifen können:

- Sie können eine Azure SQL-Datenbank in Ihrem eigenen Azure-Mandanten bereitstellen und die BYOD-Funktion (Bring Your Own Database) zum Synchronisieren von Daten verwenden. Weitere Informationen finden Sie unter [Eigene Datenbank nutzen (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).

- Sie können Dataverse Integration zum Synchronisieren ausgewählter Entitäten in die Dataverse Datenbank verwenden. Weitere Informationen finden Sie in den [Dataverse-Tabellen](hr-developer-entities.md). 

## <a name="how-often-is-my-production-database-backed-up"></a>Wie oft wird meine Produktionsdatenbank gesichert? 

Datenbanken werden durch automatische Sicherungen mit den folgenden Frequenzen geschützt:

| Art der Sicherung | Häufigkeit |
| --- | --- |
| Vollständige Datenbank-Sicherung | Wöchentlich |
| Differenzielle Datenbanksicherung | Alle 12-24 Stunden |
| Transaktionsprotokollsicherung | Alle 5 bis 10 Minuten |

Microsoft verfügt über ausreichende Sicherungen, um die Point-in-Time-Wiederherstellung (PITR) innerhalb der letzten 14 Tage zu ermöglichen. 

Weitere Informationen über Sicherungen finden Sie unter  [Informationen zu automatischen SQL-Datenbanksicherungen](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database). 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>Kann ich eine Kopie der Sicherung meiner Produktionsdatenbank anfordern? 

Nr. Sie können jedoch eine Datenbankaktualisierungsdienstanforderung senden, um Ihre Produktionsumgebung in Ihre Sandbox-Umgebung zu kopieren. Sie können eine Azure SQL-Datenbank in Ihrem eigenen Azure-Mandanten bereitstellen und die BYOD-Funktion zum Synchronisieren von Daten aus Ihrer Produktionsumgebung verwenden. Weitere Informationen finden Sie unter [Eigene Datenbank nutzen (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database). 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>Wie verschiebe ich meine Sandbox-Umgebung für die Inbetriebnahme in die Produktion? 

Da keine Kopierfunktion zum Verschieben Ihrer Umgebung von einer Sandbox in eine Produktionsumgebung verfügbar ist, müssen Sie Datenpakete verwenden, um Daten in Ihre Produktionsumgebung zu verschieben.  

Wir empfehlen, während des gesamten Projekts eine übersichtliche Liste der in Ihrer Sandbox konfigurierten Entitäten zu führen. Testen Sie anschließend den Prozess der Umstellung und Migration aller für Ihre Inbetriebnahme erforderlichen Datenpakete. Sie müssen alle Datenpakete manuell in die Produktionsumgebung verschieben, wenn Sie bereit sind, live zu gehen. 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>Was soll ich tun, wenn meine Produktionsumgebung nicht verfügbar ist? 

Befolgen Sie die unter  [Produktionsausfall melden](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage) beschriebenen Schritte. 

 ## <a name="see-also"></a>Siehe auch

 [Liveschaltung vorbereiten](hr-admin-go-live-prepare.md)
