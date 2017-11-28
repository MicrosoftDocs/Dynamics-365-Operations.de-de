---
title: Power BI-Weiterbildung
description: "In diesem Thema wird der Power BI-Weiterbildungsinhalt beschrieben. Es wird erläutert, wie Sie auf die Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 895cc28cbbdf4ef33c55bc5732e3433d319dca6d
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="learning-power-bi-content"></a>Power BI-Weiterbildung

[!include[banner](../includes/banner.md)]

In diesem Thema wird der **Weiterbildungs**-Inhalt für Microsoft Power BI beschrieben. Es wird erläutert, wie Sie auf den Inhalt zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt

Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Juli 2017) verwenden, können Sie den **Weiterbildungs**-Inhalt in der freigegebenen Anlagenbibliothek in Microsoft Dynamics Lifecycle Services (LCS) suchen. Weitere Informationen dazu, wie Sie Power BI-Inhalte herunterladen und in Ihrer Organisation implementieren, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md). Um eine Vorführung anzusehen, die zeigt, wie der Power BI-Inhalt impementiert wird, zeigen Sie den Office Mix [Power BI-Inhalt von Microsoft und Ihren Partnern in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) an.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI Inhalt enthalten sind

Die Berichte, die im **Weiterbildungs**-Inhalt von Power BI enthalten sind, haben Diagramme und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                | Inhalt |
|-----------------------|----------|
| Überblick über die Weiterbildung     | Zusammenfassung der anderen Berichte |
| Kurs-Analyse       | Erfassung nach Lagerplatz, Teilnehmer nach Status, Kurse nach Typ pro Unternehmen und Kursanwesenheit nach Stelle |
| Erfassungsanalyse | Steuernummer |
| Kurstypen          | Kurstypen nach Qualifikation |
| Kursleiteranalyse   | Verhältnis von Kurse zu Kursleiter, Anzahl Kursleiter, Kurse vom Kursleiter, Kurse pro Kursleiter und Kursagenda nach Kursleiter |
| Angebotene Kurse       | Liste von Kursen |
| Kurs-Design        | Kursagenda |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

Die folgenden Daten werden verwendet, um die Berichte im **Weiterbildungs**-Inhalt von Power BI zu füllen. Diese Tabelle zeigt die Entitäten, auf denen der Inhalt basiert.

| Entität           | Inhalt                                                         | Beziehungen mit anderen Entitäten |
|------------------|------------------------------------------------------------------|-----------------------------------|
| Kalender-Gegenkonto  | Kalendergegenkonten zu den Segmentberichten                                | Kursagenda, Kursteilnehmer |
| Unternehmen          | Unternehmen, nach denen Berichte gefiltert werden können                                   | Kursagenda, Kursteilnehmer |
| Kurs           | Kurs, Beschreibung, Kursleitername, Standort und Status | Kursagenda, Kursteilnehmer, Kurs-Qualifikation |
| Kursagenda    | Kursprogrammen, Kurs und Start- und Endzeiten                          | Unternehmen, Kalender-Gegenkonto, Datum, Kurs |
| Kursteilnehmer | Name, Status, Einzelvorgang und Erstzulassung                         | Unternehmen, Kalender-Gegenkonto, Datum, Kurs, Demographie, Beschäftigung, Kurs, Mitarbeitername, Mitarbeitertitel, Stelle, Position |
| Kurs-Qualifikation     | Qualifikation, Fähigkeitstyp und Level                                     | Kurs |
| Datum             | Tage, Wochen, Monate und Jahre                                   | Kursagenda, Kursteilnehmer |
| Demografische Daten     | Geburtsdatum, Geschlecht, Familienstand und Nationalität         | Kursagenda, Kursteilnehmer |
| Anstellung       | Startdatum, Enddatum und Umbuchungsdatum                        | Kursagenda, Kursteilnehmer |
| Stelle              | Funktion, Typ und Titel                                        | Kursagenda, Kursteilnehmer |
| Position         | Position, Titel und FTE                  | Kursagenda, Kursteilnehmer |
| Mitarbeitername    | Vorname, Nachname, vollständiger Name                             | Kursteilnehmer |
| Mitarbeitertitel   | Titel- und Dienstalter                                         | Kursteilnehmer |

Diese Entitäten wurden verwendet, um berechnete Messungen im Datenmodell zu erstellen. Diese berechneten Messungen werden verwendet, um die Messdaten (KPIs) und Berichte zu erstellen, die im Inhalt verwendet werden. Wenn Sie zusätzliche Berechnungen in Ihren Berichten und Dashboard einbeziehen möchten, können Sie die PBIX-Datei von LCS herunterladen und bearbeiten. Diese Datei ist das Standarddatenmodell, das verwendet wurde, um den Inhalt zu erstellen. Nachdem Sie die Änderungen vorgenommen haben, können Sie ein Organisations-Inhaltspaket und ein Dashboard erstellen, die die von Ihnen hinzugefügten Informationen enthalten.

