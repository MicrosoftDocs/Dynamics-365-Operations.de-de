---
title: Dynamics 365 Human Resources-Infrastrukturzusammenführung – Aktualisierung auf Version 10.0.25
description: Dieses Thema enthält Informationen zu Microsoft Dynamics 365 Human Resources-Version 10.0.25, das die erste Welle von Funktionen in der Infrastrukturzusammenführung bringt.
author: twheeloc
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a80bedd0224f1e31dfec4e9f4c39ad1ed75d7f2f
ms.sourcegitcommit: 948978183a1da949e35585b28b8e85a63b6c12b1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2022
ms.locfileid: "8024566"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Dynamics 365 Human Resources-Infrastrukturzusammenführung – Aktualisierung auf Version 10.0.25

Die Version 10.0.25 bringt die erste Welle von Funktionen in der Infrastrukturzusammenführung. Während der Infrastrukturzusammenführung wird Microsoft Dynamics 365 Human Resources mit der Infrastruktur für Finanzen und Betrieb zusammengeführt. Es wird jedoch weiterhin als eigenständige Anwendung lizenziert, wie Dynamics 365 Finance und Dynamics 365 Supply Chain Management. Weitere Informationen zur Infrastrukturzusammenführung finden Sie unter [Dynamics 365 Human Resources Häufig gestellte Fragen zum Zusammenführen von Infrastrukturen](../human-resources/hr-infrastructure-merge-faq.md).

Die Zusammenführung bietet den Benutzern von Human Resources auf folgende Weise Konsistenz:

- [Umgebungsverwaltung und Integrationen sind zwischen Human Resources- und Apps für Finanzen und Betrieb konsistent.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Umgebungen verwalten in Microsoft Dynamics Lifecycle Services, Problemsuche und Regression Suite Automation Tool.
    - Es gibt eine einzige Codebasis, in der neue Funktionen für Human Resources als Teil des regulären One-Version-Aktualisierungsprozesses veröffentlicht werden.
    - Die Art und Weise, wie Upgrades, Updates und Hotfixes auf Umgebungen angewendet werden, ist konsistent.

- [Erweiterungsoptionen wurden verbessert.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options.md)

    - Sie können Microsoft Power Platform-Tools nach Bedarf weiter ausweiten.
    - Sie können die Funktionalität über Formulare, Tabellen, Methoden und Anwendungsprogrammierschnittstellen (APIs) erweitern.
    - Sie können Entitäten erstellen und erweitern.

    Weitere Informationen zu den verfügbaren Erweiterungsoptionen finden Sie unter [Übersicht über die Erweiterbarkeit in Dynamics 365](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

- [Erstellen Sie einen Satz von Personalfunktionen in Dynamics 365.](/dynamics365-release-plan/2021wave2/human-resources/create-one-set-human-resources-capabilities-within-dynamics-365.md)

    In der Version 10.0.25 wurden funktionale Fähigkeiten, die nur in Human Resources vorhanden waren, in der Infrastruktur für Finanzen und Betrieb verfügbar gemacht. Damit Kunden diese Funktionen in einer Umgebung für Finanzen und Betrieb nutzen können, müssen die folgenden Human Resources-Funktionen in Funktionsverwaltung aktiviert werden.

    | Funktionsname | Übersicht | Status freigeben | 
    |--------------|----------|----------------| 
    | Berechnung der Dienstjahre | Eine Einstellungsoption lässt Sie das Datum auswählen, das für die **Dienstjahre**-Berechnung verwendet wird. | Allgemein verfügbar | 
    | Verbesserungen der Workflow-Umgebung | Diese Funktion bietet eine verbesserte Benutzererfahrung für Workflow-Übermittlungen und -Genehmigungen. | Allgemein verfügbar | 
    | Leistungsbeurteilungen drucken | Sie können Leistungsbeurteilungen im PDF-Format ausdrucken. | Allgemein verfügbar | 
    | Benutzerdefinierte Links im **Manager-Self-Service** | Sie können benutzerdefinierte Links erstellen, die im **Ähnliche Links**-Abschnitt von **Manager-Self-Service** angezeigt werden. | Allgemein verfügbar | 
    | Ansicht für unternehmensübergreifende Vergütung | Benutzer können Vergütungspläne in **Manager-Self-Service** über alle juristischen Personen hinweg anzeigen, ohne das Unternehmen wechseln zu müssen. | Allgemein verfügbar | 
    | Mehrere Vergütungsstufen nach Stellen konfigurieren\*&dagger; | Stellen unterstützen jetzt mehrere Vergütungsstufen. | Vorschau | 
    | Aufgabenverwaltung\* | Sie können Checklisten und Aufgaben für den Onboarding-, Offboarding- und Übergangsprozess erstellen. | Vorschau | 
    | Optimierter Mitarbeitereintrag | Diese Funktion bietet eine aktualisierte Benutzererfahrung auf der bestehenden **Arbeitskraft**-Seite. | Vorschau | 
    | Verbesserungen der Benutzererfahrung für das Personalwesen | Siehe Tabelle im nächsten Abschnitt.  | Vorschau | 

\* Diese Funktion muss vor der Funktion **Verbesserungen der Human Resources-Benutzererfahrung** aktiviert werden.

&dagger; Diese Funktion kann nicht deaktiviert werden, nachdem sie aktiviert wurde.

## <a name="human-resource-user-experience-enhancements"></a>Verbesserungen der Human Resource-Benutzererfahrung

| Funktionsname | Übersicht | 
|--------------|----------| 
| Beschäftigung löschen | Sie können die Beschäftigung eines Mitarbeiters löschen. | 
| Stellenfamilien | Sie können eine Gruppe von Stellen verfolgen, die ähnliche Tätigkeiten enthalten und ähnliche Ausbildung, Fähigkeiten, Kenntnisse und Fachkenntnisse erfordern. | 
| Zusätzliche Beschäftigungsfelder | Folgende Felder wurden hinzugefügt: **Beschäftigungskategorie**, **Beschäftigungsverhältnis** und **Arbeitsverhältnis**. | 
| **Arbeitskräfte ohne Beschäftigung**-Seite | Auf einer Seite wird eine Liste von Arbeitskräften angezeigt, die keinen Beschäftigungsdatensatz haben. | 
| Aktualisierung der Benutzererfahrung der Positionsdimension | Es gibt eine verbesserte Benutzererfahrung für die Zuweisung von Positionsdimensionen pro juristischer Person. | 
| Adressänderungen im Arbeitsbereich **Personalverwaltung** | Diese Funktion bietet die Anzahl aller Adressänderungen, die während einer bestimmten Anzahl von Tagen aufgetreten sind, wie auf der Seite **Personalverwaltungsparameter** angegeben. | 
| Datensätze im Arbeitsbereich **Personalverwaltung** ablaufen lassen | Diese Funktion bietet eine Liste von Elementen für Zertifikate, Ausweise, Bewährungen, Screenings oder Tests, die abgelaufen sind oder ablaufen werden. | 
| **Validierung der Positionshierarchie**-Seite | Es erfolgt eine Prüfung auf Zirkelbezüge in der Positionshierarchie. | 
| Länderspezifische Gehaltsinformationen | Zusätzliche Abrechnungsfelder stehen je nach Land oder Region der juristischen Person, in dem/der die Arbeitnehmer beschäftigt sind, auf der **Arbeitskräftebeschäftigung**-Seite der zur Verfügung. | 
| Verbesserungen der Compliance-Berichte | Für EEO-1, Vets 4212 und OSHA300a sind zusätzliche Berichtsoptionen verfügbar. | 
| Updates für den Arbeitsbereich **Personalverwaltung** | Es wurden Updates vorgenommen, um Adressänderungen und ablaufende Datensätze nachzuverfolgen. Zusätzlich listen neue Registerkarten Arbeitskraft- und Positionsaktionen auf. | 
