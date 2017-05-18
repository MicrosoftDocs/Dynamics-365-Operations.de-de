---
title: Rekrutierungs-Power BI-Inhalt
description: "In diesem Thema wird der Dynamics 365 for Operations - Recruiting Power BI-Inhalt beschrieben. Es wird zudem beschrieben, wie das Dashboard und die Berichte, die im Inhaltspaket enthalten sind, verwendet werden und enthält Informationen zum Datenmodell und den Entitäten, die verwendet werden, um das Inhaltspaket zu erstellen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 15780e7db5867a2f6a484ceb663e617345c033c2
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="recruiting-power-bi-content"></a>Rekrutierungs-Power BI-Inhalt

[!include[banner](../includes/banner.md)]


In diesem Thema wird der Dynamics 365 for Operations - Recruiting Power BI-Inhalt beschrieben. Es wird zudem beschrieben, wie das Dashboard und die Berichte, die im Inhaltspaket enthalten sind, verwendet werden und enthält Informationen zum Datenmodell und den Entitäten, die verwendet werden, um das Inhaltspaket zu erstellen.

<a name="accessing-the-content-pack"></a>Zugreifen auf das Inhaltspaket
--------------------------

Sie finden das Recruiting-Inhaltspaket in der Bibliothek für freigegebene Anlagen in Microsoft Dynamics Lifecycle Services (LCS). Weitere Informationen dazu, wie Sie Inhalte herunterladen und mit Ihrem Microsoft Dynamics 365 for Operations verbinden, finden Sie unter [Power Bi Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Berichte, die im Paket enthalten sind
Nachdem Sie das Inhaltspaket mit Ihren Dynamics 365 for Operations Daten verbunden haben, zeigen das Dashboard und die Berichte Ihre Organisationsdaten an. Wenn Sie bisher noch nie Microsoft Power BI verwendet haben, finden Sie weitere Informationen unter [Erste Schritte in Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Die Berichte, die im Paket enthalten sind, haben Diagrammen und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                       | Inhalt                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Bewerber-Analyse           | Bewerber nach Einzelvorgang, Bewerberquellen, Bewerber nach Lagerplatz und Gesamtanzahl Bewerber           |
| Bewerberstatus             | Bewerber nach Typ und Status und Bewerberstatus                                                    |
| Bewerber-Demographie       | Bewerber nach Alter und Geschlecht und Bewerber über Bildungsgrad und Status                             |
| Rekrutierungsanalyse          | Netto-Anstellungs-Verhältnis, durchschnittlichen Tage Projekt einzustellenden, Prozentsatz- ungültige Mieten und Rekrutierungskosten                    |
| Rekrutierungsprojektanalyse | Personalbeschaffungsprojekte Nummer, durch Öffnungen Personalbeschaffungsprojekt und Bewerber über Personalbeschaffungsprojekt |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Dynamics 365 for Operations-Daten werden für die Berichte des Recruiting-Inhaltspakets verwendet. Die folgende Tabelle zeigt die Entitäten, auf denen das Paket basiert.

| Entität                          | Inhalt                                                         | Beziehungen mit anderen Entitäten                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recruiting\_Applicant           | Bewerber, eingestellte Bewerber, Netto-Anstellungs-Verhältnis und Kosten          | Recruiting\_ApplicantName Recruiting\_Company Recruiting\_CalendarOffset Recuriting\_Date Recruiting\_GeographicLocation Recruiting\_Demographics Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject                                |
| Recruiting\_ApplicantName       | Vorname, Nachname, vollständiger Name des Bewerbers                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_CalendarOffset      | Kalendergegenkonten zu den Segmentberichten                                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Company             | Unternehmen, nach denen Berichte gefiltert werden können                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Date                | Tage, Wochen, Monate und Jahre                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Demographics        | Geburtsdatum, Geschlecht, Familienstand und Nationalität         | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_EmployedApplicant   | Bewerber, Leistung, Startdatum und Bewerbertyp           | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_ApplicantName Recruiting\_Employment Recruiting\_Performance Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject          |
| Recruiting\_Employment          | Startdatum, Enddatum und Umbuchungsdatum                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_GeographicLocation  | Ort, Postleitzahl, Landkreis und Bundesland oder Kanton.                 | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Job                 | Funktion, Typ und Titel                                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Media               | Bewerberquelle                                             | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Performance         | Bewertung, Beschreibung und Bewertungsmodell                            | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_RecruitmentProject  | Projektbeschreibung, Projektstatus und Öffnungen                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_TerminatedApplicant | Gesperrte Bewerber, Grund, Leistung und Kündigungsdatum | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_Performance Recruiting\_Demographics Recruiting\_Employment Recruiting\_Media Recruiting\_RecruitmentProject Recruiting\_ApplicantName |

Diese Entitäten wurden verwendet, um berechnete Messungen zu erstellen. Diese berechneten Messungen werden verwendet, um die Messdaten (KPIs) und Berichte zu erstellen, die im Inhaltspaket verwendet werden. Wenn Sie zusätzliche Berechnungen in Ihren Berichten und Dashboard einbeziehen möchten, können Sie die Recruiting.pbix Datei von LCS herunterladen und bearbeiten. Diese Datei ist das Standarddatenmodell, das verwendet wurde, um das Inhaltspaket zu erstellen. Nachdem Sie die Änderungen vorgenommen haben, können Sie ein Organisations-Inhaltspaket und ein Dashboard erstellen, die die von Ihnen hinzugefügten Informationen enthalten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





