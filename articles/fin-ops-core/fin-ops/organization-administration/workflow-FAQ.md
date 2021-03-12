---
title: Workflow-FAQs
description: Diese Thema enthält Antworten auf häufig gestellte Fragen zum Workflowsystem.
author: ChrisGarty
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58aa4a6d313a78e88c2858637d6de167895ec534
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797390"
---
# <a name="workflow-faq"></a>Workflow-FAQs

[!include [banner](../includes/banner.md)]

Diese Thema enthält Antworten auf häufig gestellte Fragen zum Workflowsystem.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Warum erhalte ich mehrere Benachrichtigungen, wenn eine Arbeitsaufgabe abgelehnt wird?
Wenn eine Arbeitsaufgabe abgelehnt wird, erscheint die Arbeitsaufgabe als wegen Ablehnung beendet. Dem Ersteller wird eine andere Arbeitsaufgabe erstellt und zugewiesen. Das bedeutet, dass eine Benachrichtigung zur abgelehnten Arbeitsaufgabe an den Ersteller und eine separate Benachrichtigung an den Benutzer gesendet wird, dem die neue „Änderung angefordert“-Arbeitsaufgabe zugewiesen ist. 

Jede Benachrichtigung gilt für eine andere Arbeitsaufgabe, die Ähnlichkeit kann jedoch zu Unklarheiten führen. Wir suchen nach Wegen, dies in einer späteren Versionen zu verbessern.

## <a name="why-are-my-workflow-exports-failing"></a>Warum schlagen meine Workflowexporte fehl?
Derzeit gibt es eine Einschränkung der Workflowexportfunktion, durch die Workflownamen 48 Zeichen nicht überschreiten können. Das Verwenden eines Namens, der länger als 48 Zeichen ist, kann zu einem „Fehler beim Authentifizieren der Anforderung durch Server“ führen und/oder verhindern, dass eine Datei ohne Dateityp exportiert wird. Der folgende Blog-Beitrag enthält weitere Einzelheiten, [Fehlerbehebung beim Workflow-Export](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Kann der Übermittler eines Workflows auch den Workflow genehmigen?
Ja, ein Antragsteller eines Workflows kann den Workflow kann genehmigen, wenn er so konfiguriert wird. Um dieses Verhalten zu verhindern, legen Sie **Systemverwaltung > Workflow > Workflow-Parameter > Allgemein > Genehmiger > Genehmigung durch Antragsteller nicht zulassen** auf **Ja** fest.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Kann ich Warnungen zu Workflows hinzufügen, um Benachrichtigungen für Benutzer verfügbar zu machen?
Nachfolgend sind einige wesentliche Konzepte, um Warnungen für Workflows zu beachten, um Benachrichtigungen zu erhalten:
- Warnungen versus Workflowbenachrichtigungsmechanismen
    - Warnungen können für Rekordänderungen eingerichtet werden. Workflows ändern Datensätze, daher ist es möglich, eine Warnung einzurichten, die einer Datensatzänderung zugeordnet wird, die durch einen Workflow verursacht werden. Da jedoch Workflow verschiedene integrierte Benachrichtigungsoptionen haben, ist die die Verwendung von Warnungen nicht ideal.
- Standardbenachrichtigungen vom Workflow 
    - Workflows haben integrierte E-Mail-Benachrichtigungen. Ein Debitor kann die Benachrichtigungen konfigurieren, sodass die Benutzer gesendete E-Mails sind. Diese Benachrichtigungen enden nicht in den Aktivitätscenternachrichten für Benutzer.
    - In einer zukünftigen Aktualisierung werden wir die Aktivitätscenternachricht hinzufügen, damit Benutzer einem Workflow-Arbeitselement zugewiesen werden. 
- Benachrichtigungen Workflows hinzufügen
    - Aktivitätscenternachrichten können für bestimmte Benutzer erstellt werden, wie eine Nachricht, die von einem früheren Workflow in X++ erstellt wurden.
    - [Workflows haben Geschäftsereignisse](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow), die der Kunde zum Auslösen von Flows verwenden könnte, haben die gesuchten Benachrichtigungen.   

Zusammenfassend lässt sich sagen, dass, wenn ein Benutzer nicht die richtige Benachrichtigung vom Action Center erhält, wenn ihm ein Workflow-Workitem zugewiesen wird, dann nutzen Sie [Workflow-Geschäftsereignisse](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) mit Microsoft Power Automate, um zusätzliche oder andere Benachrichtigungen bereitzustellen.

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a>Warum kann der Workflow-Editor nicht unter AD FS gestartet werden?
Wenn der Workflow-Editor unter Active Directory-Verbunddiensten (AD FS) in einer aktualisierten Umgebung ausgeführt wird, kann er möglicherweise nicht gestartet werden. Wenn dies der Fall ist, stellen Sie sicher, dass die URL "https://dynamicsaxworkfloweditor/" der Eigenschaft **Microsoft Dynamics 365 for Operations Vor Ort – Workflow – Native Anwendung** in den ADFS-Einstellungen hinzugefügt wird.

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a>Warum erhalte ich SQL-Deadlocks bei der Workflow-Verarbeitung? 
Der Standardfeldwert für das Feld **Anzahl der Workflow-Items pro Batch** auf der Seite **Workflow-Parameter** ist 0. Ein Wert von 0 bewirkt, dass sich der Standardwert auf 20 Elemente pro Stapel ändert. Seien Sie bei der Anpassung dieses Wertes vorsichtig, da eine hohe Anzahl von Elementen pro Batch (> 40) zu SQL-Deadlocks führen kann.

## <a name="what-is-the-workflow-enhanced-error-feature"></a>Was ist die Workflow Enhanced Error-Funktion?
Die Funktion Workflow Enhanced Error in Version 10.0.13 fügt Fehlercodes hinzu, um verschiedene Klassen von Workflowfehlern zu unterscheiden. Die gemeldeten Fehlermeldungen ähneln sich größtenteils mit geringfügigen Unterschieden, um sie zu verdeutlichen.
