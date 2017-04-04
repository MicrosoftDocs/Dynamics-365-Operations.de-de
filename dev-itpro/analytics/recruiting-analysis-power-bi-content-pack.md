---
title: Rekrutierungsenergie BIinhalt
description: "In diesem Thema wird das Dynamics 365 - Rekrutierungsenergie für Arbeitsgänge BIinhalt. Es erläutert, wie auf die Berichte, die im Paket enthalten inhaltliche sind, und enthält Informationen zum Datenmodell und die Entitäten, die verwendet wurde, um das Inhaltstext Pack zu erstellen."
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>Rekrutierungsenergie BIinhalt

In diesem Thema wird das Dynamics 365 - Rekrutierungsenergie für Arbeitsgänge BIinhalt. Es erläutert, wie auf die Berichte, die im Paket enthalten inhaltliche sind, und enthält Informationen zum Datenmodell und die Entitäten, die verwendet wurde, um das Inhaltstext Pack zu erstellen.

<a name="accessing-the-content-pack"></a>Zugreifen des das Content Packs
--------------------------

Sie können das einziehende Inhaltstext Pack in der Bibliothek der kommenden Anlagen in den Microsoft Dynamics Lifecycle Services (LCS) suchen. Weitere Informationen dazu, wie das herunterlädt Inhaltstext Pack und es für Ihr Microsoft Dynamics 365 für Arbeitsgänge, Daten finden Sie in BIinhalt herstellt [Energie Kreditbriefen von Microsoft und von den Partnern]( power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Berichte, die im Paket enthalten inhaltliche sind
Nachdem das Inhaltstext Pack für Ihr Dynamics 365 für Arbeitsgangsdaten verbunden wurde, zeigen die Berichte die Daten der Organisation an. Wenn Sie nicht Microsoft-Energie vor BI verwendet haben, können Sie dieser auf mehr zu erfahren [geführt, Seite für Leistung BI] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData) erfahrend. Die Berichte, die im Paket enthalten inhaltliche werden, weisen den Diagrammen und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                       | Inhalt                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Bewerber-Analyse           | Bewerber nach Einzelvorgang, Bewerberquellen, Bewerber nach Lagerplatz und Gesamtanzahl Bewerber           |
| Bewerberstatus             | Bewerber nach Typ und Status und Bewerberstatus                                                    |
| Bewerber-Demographie       | Bewerber nach Alter und Geschlecht und Bewerber über Bildungsgrad und Status                             |
| Rekrutierungsanalyse          | Nettomiet-Verhältnis, durchschnittlichen Tage Projekt einzustellenden, Prozentsatz- ungültige Mieten und Rekrutierungskosten                    |
| Personalbeschaffungsprojekt-Analyse | Personalbeschaffungsprojekte Nummer, durch Öffnungen Personalbeschaffungsprojekt und Bewerber über Personalbeschaffungsprojekt |

Sie können die und die Kacheln Diagramme in diesen Erklärungen Stift und die Diagramme und die Kacheln das Dashboard filtern. Weitere Informationen dazu, wie und Energie Stift in finden Sie BI, gefiltert [Dient zum Erstellen und Konfigurieren eines Dashboard] (https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Dynamics 365 für Arbeitsgangsdaten wird verwendet, um die Berichte im einziehenden das Content Pack aufzufüllen. Die folgende Tabelle enthält die von Entitäten, dass das Inhaltstext Pack auf Grundlage war.

| Entität                          | Inhalt                                                         | Beziehungen mit anderen Entitäten                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Rekrutierungs Bewerber           | Bewerber, eingestellte Bewerber, Netzwerkmiet-Verhältnis und Kosten          | Rekrutierungs__ent_dict_PLACEHOLDER \_, das\_\_Personalbeschaffung durchführt Datum\_\_Recuriting\_\_\_\_Personalbeschaffung durchführt\_\_Personalbeschaffung durchführt\_\_Personalbeschaffung durchführt\_\_einrücken\_\_Personalbeschaffung durchführt                                |
| Rekrutierungs__ent_dict_PLACEHOLDER \_       | Bewerbervorname, -Nachname und -vollständiger Name                   | \_Rekrutierungs Bewerber, der\_EmployedApplicant Personalbeschaffung durchführt\_TerminatedApplicant Personalbeschaffung durchführt                                                                                                                                                               |
| Rekrutierungs__ent_dict_PLACEHOLDER \_      | Kalendergegenkonten zu den Segmentberichten                                | \_Rekrutierungs Bewerber, der\_EmployedApplicant Personalbeschaffung durchführt\_TerminatedApplicant Personalbeschaffung durchführt                                                                                                                                                               |
| \_Rekrutierungs Unternehmen             | Unternehmen, z von Berichten nach filtern                                   | \_Rekrutierungs Bewerber, der\_EmployedApplicant Personalbeschaffung durchführt\_TerminatedApplicant Personalbeschaffung durchführt                                                                                                                                                               |
| \_Rekrutierungs Datum                | Tagen, Wochen, Monaten und Jahre                                   | \_Rekrutierungs Bewerber, der\_EmployedApplicant Personalbeschaffung durchführt\_TerminatedApplicant Personalbeschaffung durchführt                                                                                                                                                               |
| Rekrutierungs \_Demographie        | Geburtsdatum, Geschlecht, Familienstand Nationalität und         | \_Rekrutierungs Bewerber, der\_EmployedApplicant Personalbeschaffung durchführt\_TerminatedApplicant Personalbeschaffung durchführt                                                                                                                                                               |
| Rekrutierungs__ent_dict_PLACEHOLDER \_   | Bewerber, Leistung, Startdatum und Bewerbertyp           | \_Rekrutierungs Unternehmen, das in\_CalendarOffset Personalbeschaffung durchführt\_Datum Personalbeschaffung durchführt\_GeographicLocation Personalbeschaffung durchführt\_ApplicantName Personalbeschaffung durchführt\_Beschäftigung Personalbeschaffung durchführt\_Leistung Personalbeschaffung durchführt\_Einzelvorgang Personalbeschaffung durchführt\_Medien einrücken\_RecruitmentProject Personalbeschaffung durchführt          |
| Rekrutierungs Beschäftigung \_          | Startdatum, Enddatum und Umbuchungsdatum                        | \_Rekrutierungs Bewerber, der\_EmployedApplicant Personalbeschaffung durchführt\_TerminatedApplicant Personalbeschaffung durchführt                                                                                                                                                               |
| Rekrutierungs__ent_dict_PLACEHOLDER \_  | Ort, Postleitzahl, Landkreis und Bundesland oder Kanton.                 | \_Rekrutierungs Bewerber, der\_EmployedApplicant Personalbeschaffung durchführt\_TerminatedApplicant Personalbeschaffung durchführt                                                                                                                                                               |
| \_Rekrutierungs Stelle                 | Funktion, Typ und Titel                                        | \_Rekrutierungs Bewerber, der\_EmployedApplicant Personalbeschaffung durchführt\_TerminatedApplicant Personalbeschaffung durchführt                                                                                                                                                               |
| Medien Rekrutierungs \_               | Quelle Bewerbern                                             | \_Rekrutierungs Bewerber, der\_EmployedApplicant Personalbeschaffung durchführt\_TerminatedApplicant Personalbeschaffung durchführt                                                                                                                                                               |
| \_Rekrutierungs Leistung         | Bewertung, Beschreibung und Bewertungsmodell                            | \_Rekrutierungs Bewerber, der\_EmployedApplicant Personalbeschaffung durchführt\_TerminatedApplicant Personalbeschaffung durchführt                                                                                                                                                               |
| Rekrutierungs__ent_dict_PLACEHOLDER \_  | Projektbeschreibung Projektstatus, und Öffnungen                | \_Rekrutierungs Bewerber, der\_EmployedApplicant Personalbeschaffung durchführt\_TerminatedApplicant Personalbeschaffung durchführt                                                                                                                                                               |
| Rekrutierungs__ent_dict_PLACEHOLDER \_ | Gesperrte Bewerber, Grund, Leistung und Kündigungsdatum | \_Rekrutierungs Unternehmen, das in\_CalendarOffset Personalbeschaffung durchführt\_Datum Personalbeschaffung durchführt\_GeographicLocation Personalbeschaffung durchführt\_Leistung Personalbeschaffung durchführt\_Demographie Personalbeschaffung durchführt\_Beschäftigung Personalbeschaffung durchführt\_Medien einrücken\_RecruitmentProject Personalbeschaffung durchführt\_ApplicantName Personalbeschaffung durchführt |

Diese wurden Entitäten verwendet, um berechnete Kennzahlen zu erstellen. Diese berechneten Kennzahlen, werden dann die Leistungskennzahlen (KPIs) und Berichten zu verwendet, die in das Content Pack verwendet werden. Wenn zusätzliche Berechnungen in Ihren Berichten und Dashboard einbeziehen möchten, können Sie die Recruiting.pbix-Datei der Kreditbriefe herunterladen und ändern. Diese Datei ist das Standarddatmodell, das verwendet wurde, um das Inhaltstext Pack zu erstellen. Wenn Sie die gewünschten Änderungen vorgenommen haben, können Sie ein organisatorisches Pack und ein zufriedenes Dashboard erstellen, die die Informationen enthalten, denen Sie Gäste hinzugefügt sind.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



