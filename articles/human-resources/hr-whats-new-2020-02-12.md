---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (12. Februar 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 12. Februar 2020 neu sind oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7bcb77b74f6e484d68fd57fd1680e8c2d8c82bc4
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712061"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (12. Februar 2020)

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind. Änderungen gelten für Build-Nummer 8.1.2867. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>Bestehende Einheiten CompFixedEmpls und HcmPersonImage sollten von OData aus zugänglich sein (414178)

Mit der Veröffentlichung in dieser Woche sind die Entitäten **CompFixedEmpls** und **HcmPersonImage** nun öffentlich und über ODAta verfügbar.

## <a name="delete-employment-from-common-data-service-doesnt-work-when-employment-details-arent-active-403193"></a>Das Löschen der Beschäftigung von Common Data Service funktioniert nicht, wenn die Beschäftigungsdetails nicht aktiv sind (403193)

Diese Änderung ermöglicht nun die Löschung der Beschäftigung über Common Data Service, wenn keine Angaben zur aktiven Beschäftigung vorliegen.

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>Der Workflow für die Kursregistrierung ändert den Status auf „abgeschlossen“ und Fehler nach der zweiten Genehmigung (409749)

Der Arbeitsablauf für die Kursregistrierung wurde aktualisiert, um mehrere Genehmigende zu berücksichtigen.

## <a name="in-preview"></a>Vorschau

Die folgenden Vorschaufunktionen sind am 3. Februar 2020 verfügbar:

- **Urlaubs- und Abwesenheitsfunktion** - Weitere Informationen finden Sie unter [Urlaub- und Abwesenheitsverwaltung, Vorschaufunktion](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Vorschaufunktion für das Leistungsmanagement** – Weitere Informationen, einschließlich bekannter Probleme, finden Sie unter [Übersicht über das Leistungsmanagement](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Bald verfügbar

### <a name="platform-update-32"></a>Plattformupdate 32 

Das Plattform-Update 32 wird in Kürze verfügbar sein. [Weitere Informationen zu Platform Update 32 finden Sie hier](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

### <a name="updated-common-data-service-solution"></a>Aktualisierte Common Data Service Lösung

Eine neue Common Data Service Lösung wird in Kürze mit den folgenden Änderungen verfügbar sein:

| Beschreibung | Änderung |
| ----------------------------------------- | --- |
| **Stelle/Position** Entitätsänderungen | **Kompensationsregion** hinzugefügt</br>**Finanzdimensionen** hinzugefügt |
| **Arbeitskraft** Entitätsänderungen | **Namensfolge** hinzugefügt</br>**Arbeitet von zu Hause** hinzugefügt</br>**Sprache** hinzugefügt</br>**Dienstalterdatum** hinzugefügt</br>**Jahrestag** hinzugefügt</br>**Ursprüngliches Einstellungsdatum** hinzugefügt |
| **Beschäftigung** Entitätsänderungen | **Finanzdimensionen** hinzugefügt</br>**Kündigungsgrund** hinzugefügt</br>**Kündigungsdatum** umbenannt von **Übergangsdatum**</br>**Probezeitdatum** hinzugefügt |
| **Arbeitskraftadresse** Entitätsänderungen | **Straße** hinzugefügt</br>**Adresszeile 1**, **Adresszeile 2**, und **Adresszeile 3** als veraltet markiert |
| Neue variable Vergütung-Einrichtungsentitäten | **Plantyp für variable Vergütung**</br>**Plan für variable Vergütung**</br>**Übertragungsregeln**</br>**Variable Planstufe zur Vergütung** |
| Neue **Arbeitskraftkalender-Beschäftigung** Entität | **Arbeitkraftkalender-Entität** hinzugefügt |
| Neue **Lohnpositionsdetail** Entität | **Lohnpositionsdetail** hinzugefügt |
| Neue **Titel** Entität | **Titel** hinzugefügt. Die neue Einheit **Titel** wird in den Synchronisationsprozess zwischen Human Resources und Common Data Service einbezogen. Sie wird nicht zunächst von **Job-Position** oder **Job** Entitäten referenziert. |

## <a name="see-also"></a>Siehe auch

[Neuigkeiten oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)