---
title: Rekrutierungs-Power BI-Inhalt
description: "In diesem Thema wird der Inhalt der Power BI-Personalbeschaffung beschrieben. Es wird erläutert, wie Sie auf die Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 42d7b94e655799596f478e7592a17437b336099e
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="recruiting-power-bi-content"></a>Rekrutierungs-Power BI-Inhalt

[!include[banner](../includes/banner.md)]

In diesem Thema wird der **Personalbeschaffungs**-Inhalt für Microsoft Power BI beschrieben. Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt
Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Juli 2017) verwenden, wird der Power BI-Inhalt **Personalbeschaffung** im Arbeitsbereich **Personalbeschaffungsverwaltung** angezeigt. 

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Berichte und Grafiken im Arbeitsbereich "Personalbeschaffungsverwaltung"
Der Arbeitsbereich **Personalbeschaffungsverwaltung** enthält eine Registerkarte **Analyse** . Diese Registerkarte enthält die eingebetteten Power BI-Inhalte für die Personalbeschaffung. Der Inhalt besteht aus einer Übersichtsregisterkarte und zusätzlichen Registerkarten mit Details. Die Berichte werden auf jeder Registerkarte näher erläutert.

| Bericht               | Inhalt |
|----------------------|----------|
| Überblick über die Personalbeschaffung | Zusammenfassung der anderen Berichte |
| Bewerber-Analyse   | Gesamtzahl der Bewerber; Bewerber nach Stelle, Bewerber nach Quelle, weibliche oder männliche Bewerber und Bewerber nach Standort. |
| Bewerberstatus     | Bewerber nach Typ und Status und Bewerberstatus |
| Rekrutierungsanalyse  | Nettoanstellungsrate, durchschnittliche Anstellungen pro Tag, Prozentsatz nicht erfolgreiche Rekrutierungen,  Rekrutierungskosten, Anzahl Personalbeschaffungsprojekte, Rekrutierungen angewendet und Bewerber versus offene Stellen nach Personalbeschaffungsprojekt. |

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Die folgende Tabelle zeigt die Entitäten, auf denen der Power BI Inhalt **Personalbeschaffung** basiert.

| Entität               | Inhalt                                                         | Beziehungen mit anderen Entitäten |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| Bewerber            | Bewerber, eingestellte Bewerber, Netto-Anstellungs-Verhältnis und Kosten          | Bewerbername, Unternehmen, Kalender-Gegenkonto, Datum, Standort, Demographie, Stelle, Medien, Personalbeschaffungsprojekt |
| Name des Bewerbers       | Vorname, Nachname, vollständiger Name des Bewerbers                   | Bewerber, Bewerber angestellt, Bewerber beendeter |
| Kalender-Gegenkonto      | Kalendergegenkonten zu den Segmentberichten                                | Bewerber, Bewerber angestellt, Bewerber beendeter |
| Unternehmen              | Unternehmen, nach denen Berichte gefiltert werden können                                   | Bewerber, Bewerber angestellt, Bewerber beendeter |
| Datum                 | Tage, Wochen, Monate und Jahre                                   | Bewerber, Bewerber angestellt, Bewerber beendeter |
| Demografische Daten         | Geburtsdatum, Geschlecht, Familienstand und Nationalität         | Bewerber, Bewerber angestellt, Bewerber beendeter |
| Angestellter Bewerber   | Bewerber, Leistung, Startdatum und Bewerbertyp           | Unternehmen, Kalender-Gegenkonto, Datum, Standort, Bewerbername, Anstellung, Leistung, Stelle, Medien, Personalbeschaffungsprojekt |
| Anstellung           | Startdatum, Enddatum und Umbuchungsdatum                        | Bewerber, Bewerber angestellt, Bewerber beendeter |
| Geografischer Standort  | Ort, Postleitzahl, Landkreis und Bundesland oder Kanton.                 | Bewerber, Bewerber angestellt, Bewerber beendeter |
| Stelle                  | Funktion, Typ und Titel                                        | Bewerber, Bewerber angestellt, Bewerber beendeter |
| Medien                | Bewerberquelle                                             | Bewerber, Bewerber angestellt, Bewerber beendeter |
| Leistung          | Bewertung, Beschreibung und Bewertungsmodell                            | Bewerber, Bewerber angestellt, Bewerber beendeter |
| Personalbeschaffungsprojekt  | Projektbeschreibung, Projektstatus und Öffnungen                | Bewerber, Bewerber angestellt, Bewerber beendeter |
| Beendeter Bewerber | Gesperrte Bewerber, Grund, Leistung und Kündigungsdatum | Unternehmen, Kalender-Gegenkonto, Datum, Standort, Leistung, Demografie, Anstellung, Medien, Personalbeschaffungsprojekt, Bewerbername. |

Diese Entitäten wurden verwendet, um berechnete Messungen zu erstellen. Diese berechneten Messungen werden verwendet, um die Messdaten (KPIs) und Berichte zu erstellen, die im Inhalt verwendet werden. Wenn Sie zusätzliche Berechnungen in Ihren Berichten und Dashboard einbeziehen möchten, können Sie die Recruiting.pbix Datei von Microsoft Dynamics Lifecycle Services (LCS) herunterladen und bearbeiten. Diese Datei ist das Standarddatenmodell, das verwendet wurde, um den Inhalt zu erstellen. Nachdem Sie die Änderungen vorgenommen haben, können Sie ein Organisations-Inhaltspaket und ein Dashboard erstellen, die die von Ihnen hinzugefügten Informationen enthalten.

