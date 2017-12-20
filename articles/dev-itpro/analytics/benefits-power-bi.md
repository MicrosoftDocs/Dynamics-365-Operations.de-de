---
title: "Power BI-Inhalt – Vorteile"
description: "In diesem Thema wird der Inhalt der Power BI-Vorteile beschrieben. Es wird beschrieben, wie auf die Berichte, die enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden."
author: jcart1106
manager: AnnBe
ms.date: 12/01/2017
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
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 25111ac7ae07e04bc81ac23a348464bcbe1393af
ms.contentlocale: de-de
ms.lasthandoff: 12/01/2017

---

# <a name="benefits-power-bi-content"></a>Power BI-Inhalt – Vorteile

[!include[banner](../includes/banner.md)]

In diesem Thema wird der **Vorteile**-Inhalt für Microsoft Power BI beschrieben. Es wird beschrieben, wie auf die Berichte, die enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden.

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt
Der **Vorteile**-Inhalt für Power BI wird im Arbeitsbereich **Vorteilsverwaltung** angezeigt, wenn Sie eines der folgenden Produkte verwenden:

- Microsoft Dynamics 365 for Finance and Operations (Enterprise-Edition)
- Microsoft Dynamics 365 for Talent

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI Inhalt enthalten sind
Die Berichte, die im **Vorteile**-Inhalt von Power BI enthalten sind, haben Diagramme und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                       | Inhalt                                                                                       |
|------------------------------|------------------------------------------------------------------------------------------------|
| Überblick der Vorteils-Registrierung  | Die meisten und am wenigsten registrierten Pläne, Registrierung durch Mitarbeitergruppe und ausgewählte Vorteilsplanoptionen |
| Mitarbeitervergütungen            | Mitarbeiterregistrierung nach ausgewählten Vorteilen                                                        |
                                                                                             
Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="extending-the-power-bi-content"></a>Erweitern des Power BI-Inhalts
Wenn Sie die Inhaltspacks verwenden, die in Microsoft Dynamics Lifecycle Services (LCS) verfügbar sind, können Sie großartige Analysen für Person bereitstellen, die sich nicht in Finance and Operations anmelden. Sie können diese Inhaltspakete so ändern, dass sie andere Berichte oder grafische Elemente umfassen, und die Inhaltspakete dann für die Analyse auf Ihrem Power BI.com-Mandanten veröffentlichen.

Sie können den **Vorteils**-Inhalt für Power BI in der freigegebenen Anlagenbibliothek in LCS finden. Weitere Informationen dazu, wie Sie Power BI-Inhalte herunterladen und in Ihrer Organisation implementieren, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md). Um eine Vorführung anzusehen, die zeigt, wie der Power BI-Inhalt impementiert wird, zeigen Sie den Office Mix [Power BI-Inhalt von Microsoft und Ihren Partnern in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) an.

>[!NOTE]
>Die PBIX-Dateien, die in Lifecycle Services verfügbar sind, gelten nur für Finance and Operations.

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Die folgenden Daten werden verwendet, um die Berichte im **Vorteile**-Inhalt von Power BI zu füllen. Diese Tabelle zeigt die Entitäten, auf denen der Inhalt basiert.

| Entität                   | Inhalt                                                                                                   | Beziehungen mit anderen Entitäten |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalender-Gegenkonto          | Kalendergegenkonten zu den Segmentberichten                                                                          | Zuweisung hinter der Position, Positionstrend, Mitarbeitertrend, ausgeschiedener Mitarbeiter |
| Unternehmen                  | Unternehmen, nach denen Berichte gefiltert werden können                                                                             | Aktuelle Vergütung, aktuelle Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Vergütung             | Lohnsatz und Häufigkeit im Zeitverlauf                                                                           | Aktuelle Vergütung, aktuelle Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Aktuelle Vergütung     | Lohnsatz und Häufigkeit ab dem aktuellen Datum                                                              | Unternehmen, Vergütung, Demographie, Einzelvorgang, Position |
| Aktuelle Position         | Positionen nach dem aktuellen Datum, aufgerechtet nach Vollzeit (FTE), offen Positionen und offenen, zu besetzenden Positionen | Stelle, Position |
| Aktueller Mitarbeiter         | Arbeitskräfte zum aktuellen Datum, Alter und Anzahl Mitarbeitende                                                         | Unternehmen, Vergütung, geografischer Standort, Mitarbeitername, Vorgesetzter, Mitarbeitertitel, Demographie, Stelle, Beschäftigung, Position, Vergütungen, |
| Datum                     | Tage, Wochen, Monate und Jahre                                                                             | Vorheringe Positionszuweisung, Positionstrend, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Demografische Daten             | Geburtsdatum, Geschlecht, Familienstand und Nationalität                                                   | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Anstellung               | Startdatum, Enddatum und Umbuchungsdatum                                                                  | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Geografischer Standort      | Ort, Postleitzahl, Landkreis und Bundesland oder Kanton.                                                           | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Stelle                      | Funktion, Typ und Titel                                                                                  | Aktuelle Position, aktueller Mitarbeiter |
| Zuordnung hinter der Position | Zuweisungsgrund, Startdatum, Enddatum und Stelle                                                           | Kalender-Gegenkonto, Datum, Stelle, Position |
| Position                 | Abteilung, FTE, Position, Titel, Positionstyp                                                        | Aktuelle Position, aktueller Mitarbeiter |
| Positionstrend           | Positionen im Zeitverlauf, FTE und Aufgabenbereich                                                                          | Kalender-Gegenkonto, Datum, Stelle, Position |
| Vorgesetzter               | Vorname, Nachname, vollständiger Name                                                                       | Aktuelle Arbeitskraft, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Ausgeschiedener Mitarbeiter      | Ausgeschiedene Mitarbeiter, Kündigungsdatum, Titel, Position und Stelle                                           | Unternehmen, Vergütung, geografischer Standort, Mitarbeitername, Vorgesetzter, Kalender-Gegenkonto, Datum Mitarbeitertitel, Demographie, Beschäftigung, Stelle, Position, Vergütungen |
| Vorteile                 | Gültigkeitsdatum, Vergütungsoption, Vergütungsplan und Vergütungstyp                                             | Aktueller Name, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Mitarbeitername            | Vorname, Nachname, vollständiger Name                                                                       | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Mitarbeitertitel           | Titel- und Dienstalter                                                                                   | Aktueller Mitarbeiter, ausgeschiedener Mitarbeiter, Mitarbeitertrend |
| Mitarbeitertrend           | Arbeitskräfte im Zeitverlauf, Mitarbeiterzahl, Unternehmen und Position                                                        | Unternehmen, Vergütung, geografischer Standort, Mitarbeitername, Vorgesetzter, Kalender-Gegenkonto, Datum Mitarbeitertitel, Demographie, Beschäftigung, Stelle, Vergütungen |

Diese Entitäten wurden verwendet, um berechnete Messungen im Datenmodell zu erstellen. Diese berechneten Messungen werden verwendet, um die Messdaten (KPIs) und Berichte zu erstellen, die im Inhalt verwendet werden. Wenn Sie zusätzliche Berechnungen in Ihren Berichten und Dashboard einbeziehen möchten, können Sie die PBIX-Datei von LCS herunterladen und bearbeiten. Diese Datei ist das Standarddatenmodell, das verwendet wurde, um den Inhalt zu erstellen. Nachdem Sie die Änderungen vorgenommen haben, können Sie ein Organisations-Inhaltspaket und ein Dashboard erstellen, die die von Ihnen hinzugefügten Informationen enthalten.

