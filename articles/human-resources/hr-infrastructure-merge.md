---
title: Dynamics 365 Human Resources Infrastruktur zusammenführen – Übersicht
description: Dieser Artikel beschreibt die Zusammenführung der Microsoft Dynamics 365 Human Resources Infrastruktur.
author: twheeloc
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e68b28bfde35b51605aa0b653265da6261b69a90
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819241"
---
# <a name="dynamics-365-human-resources-infrastructure-merge"></a>Dynamics 365 Human Resources Infrastruktur zusammenführen 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="dynamics-human-resources-365"></a>Dynamics Human Resources 365

Microsoft Dynamics 365 Human Resources bietet Tools, die HR-Teams dabei helfen, die organisatorische Agilität zu erhöhen, die Mitarbeitererfahrung zu verändern und HR-Programme zu optimieren, um einen Workplace zu erstellen, in dem Mitarbeiter und Unternehmen erfolgreich sind. Um mehr über Dynamics 365 Human Resources zu erfahren, siehe [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Transformieren Sie die Mitarbeitererfahrung.** Binden Sie Spitzenkräfte an Ihr Unternehmen, indem Sie Managern und Mitarbeitern durch vernetzte Self-Service-Erlebnisse die Möglichkeit geben, sich zu engagieren und zu wachsen.
- **HR-Programme optimieren**. Helfen Sie, die Betriebskosten zu senken, und erstellen Sie personalbezogene Programme für Urlaub und Abwesenheit, Zeit, Leistungen und Vergütung.
- **Steigern Sie die organisatorische Agilität**. Ermöglichen Sie der Personalabteilung, mit der vom Unternehmen geforderten Geschicklichkeit zu arbeiten, indem Sie Dataverse und Microsoft Power Platform verwenden, um Personaldaten zu zentralisieren und Dynamics 365 Human Resources einfach zu erweitern.
- **Einblicke in die Belegschaft entdecken**. Treffen Sie datengestützte Entscheidungen, indem Sie Personendaten auf umfangreichen Dashboards analysieren und visualisieren, die auf jedem Gerät verfügbar sind.

## <a name="human-resources-infrastructure-merge"></a>Zusammenführung der Infrastruktur von Human Resources

Dynamics 365 Human Resources ist eine eigenständige Anwendung, die derzeit eine andere Infrastruktur nutzt als andere Finanz- und Betriebs-Apps verwendet, wie z. B. Dynamics 365 Finance oder Dynamics 365 Supply Chain Management. Durch die Zusammenführung der Infrastruktur wird Dynamics 365 Human Resources in dieselbe Infrastruktur wie andere Finanz- und Betriebs-Apps gebracht.

Mehr über die Zusammenführung der Human Resources Infrastruktur erfahren Sie unter [Zusammenführung von HR-Angeboten](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers/). Antworten auf häufig gestellte Fragen finden Sie unter [Häufig gestellte Fragen zur Zusammenführung der Infrastruktur von Human Resources](./hr-infrastructure-merge-faq.md).

## <a name="customer-migration-vs-customer-merge"></a>Debitorenmigration vs. Debitorenzusammenführung

Im Rahmen der Zusammenführung der Infrastruktur wurden alle Fähigkeiten der Human Resources Anwendung in den Finanz- und Betriebsumgebungen verfügbar gemacht. Debitoren können ihre Human Resources-Umgebungen mithilfe der in Microsoft Dynamics Lifecycle Services verfügbaren Migrationstools migrieren. Optional können sie ihre Daten auch mit ihrer bestehenden Finanz- und Betriebsumgebung zusammenführen. 

Debitorenmigration und Debitorenzusammenführung unterscheiden sich wie folgt:

- **Debitorenmigration**: Das automatisierte Migrationstool wird verwendet, um eine „Migration per Shift & Lift“ (verschieben) der Debitorendatenbank von der Human Resources-Infrastruktur zur Finanz- und Betriebsinfrastruktur durchzuführen. Das Ergebnis ist eine neue Finanz- und Betriebsumgebung, die die Human Resources-Datenbank des Debitors verwendet. 
- **Debitorenzusammenführung**: Dieser zusätzliche Schritt wird von Microsoft nicht verlangt. Dies geschieht nach Ermessen und den eigenen Zeitplänen des Debitors. Während dieses Schritts werden Debitorendaten in eine vorhandene Umgebung verschoben, beispielsweise in eine Finanz- oder Project Operations-Umgebung. Dies geschieht größtenteils manuell und kann mithilfe von Datenentitäten des Datenverwaltungs-Frameworks (DMF) erledigt werden. 

## <a name="planning-a-human-resources-environment-migration"></a>Die Migration einer Human Resources-Umgebung planen

Im Rahmen der Zusammenführung der Infrastruktur müssen alle Debitoren ihre bestehenden Human Resources-Umgebungen aus der eigenständigen Infrastruktur migrieren. Um diesen Prozess zu unterstützen, empfehlen wir Ihnen, die automatisierten Migrationstools in Lifecycle Services zu verwenden, um Ihre aktuellen Umgebungen in die neue Infrastruktur zu verschieben. 

Die folgenden Abschnitte enthalten weitere Einzelheiten zur Verwendung der Lifecycle Services-Tools zum Migrieren einer eigenständigen Human Resources-Umgebung. 

Debitoren, die eine Migration planen, haben eventuell die folgenden Erwartungen:

- Alle Debitoren müssen auf eine Sandbox-Umgebung migrieren, bevor sie die Produktionsumgebung migrieren können. 
- Migrationstools ermöglichen nur die Migration von Sandbox zu Sandbox und von Produktion zu Produktion. Daher bestimmt Ihr Umgebungstyp, welche Umgebung richtig migriert werden kann. 
- Debitoren können so viele Sandboxes wie nötig migrieren, bevor sie ihre Produktionsumgebung migrieren, vorausgesetzt, ein Ziel-Sandbox-Steckplatz ist verfügbar. Debitoren können auch eine migrierte Sandbox löschen und mehrmals neu migrieren. 
- Wenn eine Sandbox-Migration fehlschlägt oder Sie von vorne beginnen möchten, können Sie eine Umgebung in der Finanz- und Betriebsinfrastruktur löschen und dieselbe Umgebung erneut migrieren.
- Die URL Ihrer Human Resources-Umgebung ist nach der Migration eine andere.
- Planen Sie für die Migration Ihrer Produktionsumgebung eine angemessene Downtime für Ihr Unternehmen ein. Der geschätzte Zeitrahmen für den Abschluss des automatisierten Migrationsprozesses beträgt drei bis vier Stunden. Der Zeitrahmen variiert je nach den Daten Ihrer Organisation. Sie sollten den Zeitaufwand für die Migration Ihrer Sandbox-Umgebungen überprüfen und Zeit für zusätzliche manuelle Aufgaben einplanen, die ausgeführt werden müssen.

> [!IMPORTANT] 
> Wenn eine Produktionsumgebung erfolgreich zur Finanz- und Betriebsinfrastruktur migriert wurde, wird die eigenständige Quell-Produktionsumgebung automatisch gelöscht. Sie sollten die migrierte Produktionsumgebung nicht löschen. 

Der Prozess für die Migration läuft größtenteils automatisch ab. Ihre Geschäftsbenutzer müssen jedoch nach der Migration einige manuelle Schritte und Überprüfungen vornehmen.

Die folgenden manuellen Schritte müssen ausgeführt werden:

- Erstellen Sie ein neues Lifecycle Services-Projekt für die Migration.
- Überarbeiten Sie alle Integrationen in Ihrer alten Umgebung für die neue Umgebung, indem Sie die Integration, ausgehend von den einzelnen Integrationskonfigurationen, auf die neue URL/Endpunkte verweisen.
- Aktualisieren Sie den Datenspeicher für eingebettete Power BI-Berichte.
- Aktualisieren Sie die Datenentitätsliste aus dem DMF-Arbeitsbereich.
- Verlinken Sie zur Unterstützung die Lifecycle Services.
- Erstellen Sie Steuerkalender.

Während des automatischen Prozesses werden die folgenden Aktionen ausgeführt und sollten überprüft werden:

- Daten:

    - Konfigurationen
    - Sicherheitsrollen (einschließlich benutzerdefinierter Rollen)
    - Workflow (einschließlich Benachrichtigungen)
    - Personalisierungen und gespeicherte Ansichten
    - Transaktionen
    - Benutzerdefinierte Felder
    - Anhänge
    - Warnungen

- Datenverwaltung – Bring your own Database (BYOD).
- Funktionsverwaltung – aktivierte/deaktivierte Funktionen.
- Eingebettete Power Apps.
- Mit Power Platform Admin Center verbundene Umgebung (nur Produktion).
- Batchaufträge.
- Für jede juristische Person wird ein leeres Sachkonto erstellt. Der Standardtyp des Wechselkurses und die Buchhaltungswährung für jedes Sachkonto werden festgelegt.
- In jeder juristischen Person wird ein neuer Kontoplan automatisch erstellt und mit der Seite **Sachkonto** erstellt. Die in Ihrer Human Resources-Umgebung konfigurierten Finanzdimensionen werden automatisch zu einer neuen Kontostruktur hinzugefügt und mit dem Sachkonto verknüpft. 

> [!NOTE]
> Als Teil des Dynamics 365 Finance-Produkts ist ein Sachkonto für die Finanz- und Betriebsinfrastruktur erforderlich. Die benutzerdefinierte Dimensionssteuerung in der eigenständigen Dynamics 365 Human Resources-Anwendung ist nicht verfügbar. Die zusammengeführte Infrastruktur für Human Resources hängt von der Finanzlogik zur Anzeige finanzieller Dimensionen im Modul **Human Resources** ab. Weitere Informationen zum Kontoplan und zu Finanzdimensionen finden Sie [hier](../finance/general-ledger/plan-chart-of-accounts.md). 

## <a name="considerations"></a>Überlegungen

- Die Migration zu Umgebungen erfolgt immer auf der neuesten allgemein verfügbaren (GA) Version. Wenn die Überprüfung Ihrer Migration für Sandbox-Umgebungen auf einer anderen Version erfolgt ist, sollten Sie, je nach Ihrem Migrations- und Testplan, eine Sandbox-Migration auf derselben Version wie Ihre Produktionsumgebung überprüfen. 
- Während der Migration werden die migrierten Umgebungen in derselben Region platziert wie die eigenständigen Human Resources-Quellumgebungen.

## <a name="licensing"></a>Lizenzierung

Es gibt in den folgenden Bereichen keine Änderungen an der Lizenzierung für Dynamics 365 Human Resources: 

- **Mindestanforderung für den Lizenzkauf**
- **Lizenzen für eine Produktions- und eine Sandbox-Umgebung**: Wenn Sie bereits über eigenständige Human Resources-Lizenzen verfügen, die eine Produktionsumgebung und eine Sandbox-Umgebung gewähren, steht die gleiche Anzahl von Lizenzen ohne zusätzliche Kosten für die Finanz- und Betriebsinfrastruktur zur Verfügung.
- **Zusätzliche Sandbox-Lizenzen**: Wenn Sie zusätzliche Sandbox-Lizenzen für die eigenständige Human Resources-Anwendung erworben haben, steht die gleiche Anzahl von Sandbox-Lizenzen ohne zusätzliche Kosten für eine Standard-Akzeptanztestumgebung (Sandbox) in der Finanz- und Betriebsinfrastruktur zur Verfügung. 
