---
title: Rekrutierungs-Power BI-Inhalt
description: In diesem Thema wird der Power BI-Inhalt zur Personalbeschaffung beschrieben. Es wird erläutert, wie Sie auf die Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: HcmRecruitmentWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b92078ca2bc89d752895bf3b4f2f3cdb2c2fd2f6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185220"
---
# <a name="recruiting-power-bi-content"></a>Rekrutierungs-Power BI-Inhalt

[!include [banner](../includes/banner.md)]

In diesem Thema wird der Microsoft Power BI-Inhalt zur **Personalbeschaffung** beschrieben. Es erläutert, wie Sie auf die Power BI-Berichte zugreifen, und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet wurden, um den Inhalt zu erstellen.

## <a name="accessing-the-power-bi-content"></a>Zugreifen auf den Power BI-Inhalt
Der **Recruiting** Power BI-Inhalt wird im Arbeitsbereich **Einstellungsverwaltung** angezeigt.

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Berichte und Grafiken im Arbeitsbereich "Personalbeschaffungsverwaltung"
Der Arbeitsbereich **Personalbeschaffungsverwaltung** enthält eine Registerkarte **Analyse**. Diese Registerkarte enthält die eingebetteten Power BI-Inhalte für die Personalbeschaffung. Der Inhalt besteht aus einer Übersichtsregisterkarte und zusätzlichen Registerkarten mit Details. Die Berichte werden auf jeder Registerkarte näher erläutert.

| Bericht               | Inhalt |
|----------------------|----------|
| Überblick über die Personalbeschaffung | Zusammenfassung der anderen Berichte |
| Bewerber-Analyse   | Gesamtzahl der Bewerber; Bewerber nach Stelle, Bewerber nach Quelle, weibliche oder männliche Bewerber und Bewerber nach Standort. |
| Bewerberstatus     | Bewerber nach Typ und Status und Bewerberstatus |
| Rekrutierungsanalyse  | Nettoanstellungsrate, durchschnittliche Anstellungen pro Tag, Prozentsatz nicht erfolgreiche Rekrutierungen,  Rekrutierungskosten, Anzahl Personalbeschaffungsprojekte, Rekrutierungen angewendet und Bewerber versus offene Stellen nach Personalbeschaffungsprojekt. |

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Die folgende Tabelle zeigt die Entitäten, auf denen der **Rekrutierungs**-Power BI-Inhalt basiert.

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