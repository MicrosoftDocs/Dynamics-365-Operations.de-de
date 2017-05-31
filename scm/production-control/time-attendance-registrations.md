---
title: Zeit- und Anwesenheitserfassung
description: "Arbeitskräfte mit Zeiterfassung können verschiedene Arten von Zeiterfassungen eingeben. Sie können sich z. B. ein- und ausstempeln sowie indirekte Aktivitäten und Abwesenheiten erfassen. In diesem Artikel beschreibt Erfassungen, ihre Berechnung, Genehmigung, und die Verwendung von Workflows sowie das Hinzufügen von Struktur und die automatisierte Genehmigung für Arbeitszeitnachweisen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, JmgCalcApprovePickDialog, JmgGroupApprove, JmgGroupCalc, JmgGroupSigningTable, JmgRegistration, JmgTimeCalcParmeters, WorkflowTableListPageRnr
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53351
ms.assetid: 885b0cdf-53d7-4cb4-92fe-da1b9e32b39f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 12193e4c266abc7bf0349ba9a78dbbbd9d00938d
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="time-and-attendance-registration"></a>Zeit- und Anwesenheitserfassung

[!include[banner](../includes/banner.md)]


Arbeitskräfte mit Zeiterfassung können verschiedene Arten von Zeiterfassungen eingeben. Sie können sich z. B. ein- und ausstempeln sowie indirekte Aktivitäten und Abwesenheiten erfassen. In diesem Artikel beschreibt Erfassungen, ihre Berechnung, Genehmigung, und die Verwendung von Workflows sowie das Hinzufügen von Struktur und die automatisierte Genehmigung für Arbeitszeitnachweisen. 

<a name="registrations"></a>Registrierungen
-------------

In Unternehmen, die Zeit und Anwesenheit verwenden, müssen Arbeitskräfte die Zeit, die sie am Arbeitsplatz arbeiten, sowie die Anwesenheit erfassen. In einigen Unternehmen müssen sich Arbeitskräfte ggf. nur ein- und ausstempeln. In anderen Unternehmen, müssen Arbeitskräfte ggf. auch den Zeitverbrauch für die tatsächlichen Aktivitäten sowie die Pausen erfassen. Arbeitszeiten und Abwesenheitszeiten sind für die folgenden Benutzer bestimmt:
-   Arbeitskräfte, die regelmäßig Zeit und Anwesenheit erfassen müssen, z. B. täglich, wöchentlich oder alle zwei Wochen.
-   Supervisor, Manager und Lohnbuchhalter, die die Erfassungen der Arbeitskräfte zur weiteren Verarbeitung berechnen, genehmigen und übertragen.

| **Hinweis**                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wenn Sie Zeit und Anwesenheit zusammen mit der Fertigungssteuerung nutzen, werden alle Erfassungen für Projekte, Projektaktivitäten, indirekte Projektvorgänge, Abwesenheitscodes und Überstunden und Gleitzeit aufgezeichnet und zur Berechnung des Lohns in beiden Modulen verwendet. |

## <a name="time-registrations-workers"></a>Zeiterfassung für Arbeitskräfte
Für die Erfassung von Zeit und Abwesenheit müssen Arbeitskräfte in dem Unternehmen, bei dem sie beschäftigt sind, als Arbeitskräfte mit Zeiterfassung eingerichtet sein.

Nach der Einrichtung können die Arbeitskräfte unterschiedliche Arten von Erfassungen eingeben.

-   Ein- und Ausstempeln beim Ankommen oder Verlassen der Arbeit.
-   Zeit und den Artikelverbrauch für Produktions-Einzelvorgänge.
-   Zeit an einer Maschine im Fertigungsbereich (wenn die Maschine als Ressource definiert wurde).

| **Hinweis**                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Einer Arbeitskraft kann automatisch die Zeiterfassungen zugewiesen werden, die im Fertigungsbereich für eine bestimmte Maschine vorgenommen wurde, wenn die Arbeitskraft die Arbeit als Assistent für die Maschine beim Start des Produktions-Einzelvorgangs auswählt. |

-   Zeiterfassungen für Projekte und Projektaktivitäten.
-   Erfassen von Projektgebühren und des Artikelverbrauchs über die jeweiligen Projektgebührerfassungen und die Projektartikelerfassungen.
-   Geplante Abwesenheit.
-   Abwesenheit durch zu späten Arbeitsantritt früher als geplant gehen.
-   Arbeitspausen, entweder manuell erfasst oder automatisch vom System berechnet.
-   Indirekte Aktivitäten, die unproduktive Aktivitäten einer Arbeitskraft während eines Arbeitstags sind. Beispiele dieser Aktivitäten sind Besprechungen oder das Säubern des Arbeitsbereichs.
-   Überstunden, die als zusätzlich geleistete Stunden entweder als Zusatzstunden, Gleitzeit oder Überstunden erfasst werden können.

## <a name="adding-clockout-registrations"></a>Hinzufügen von Ausstempelerfassungen
Wenn Arbeitskräfte vergessen, am Ende des Arbeitstags auszustempeln, können Sie die fehlende Erfassungen für diese erstellen, indem Sie einen Batchauftrag ausführen. Das System vergleicht die Einstempeluhrzeit und die Ausstempeluhrzeit gemäß dem zugeordneten Profil der Arbeitskraft und fügt automatisch die fehlenden Ausstempelerfassung ein, um die Endzeit des Profils abzugleichen. Die Ein- und Ausstempelerfassungen sind für die folgende Berechnung und die Genehmigung von Zeiterfassungen vor der Übertragung an Lohnabrechnung enorm wichtig.

## <a name="calculating-registrations"></a>Berechnen von Erfassungen
Wenn eine Arbeitskraft für Zeiterfassung eine Berechnungsgruppe zugewiesen ist, die normalerweise zu einem bestimmten Team, zu einer Schicht oder zu einer Arbeitsgruppe gehört. Der Teamleiter oder Supervisor validiert normalerweise die Erfassungen, die von Arbeitskräften vorgenommen wurden und ist daher auch die verantwortliche Person für tägliche Ausführung der Berechnung und Berechnungsgruppen. Als Teil des Berechnungsprozesses ist der Teamleiter oder Supervisor zu folgendem in der Lage:
-   Korrigieren fehlerhafter Erfassungen. Beispielsweise Ändern des Wechselcodes und Anpassen des Feedback für Produktions-Einzelvorgänge.
-   Hinzufügen von fehlenden Erfassungen. Zum Beispiel das Erstellen von Ausstempelerfassungen und Abwesenheitseinträgen.
-   Löschen von falschen Erfassungen.

Da die erfasste Zeit mit dem Zeitprofil der Arbeitskraft vor dem Berechnung der Erfassungen übereinstimmen muss, müssen Sie das Arbeitszeitprofil jede Arbeitskraft überschreiben, die eine Ausnahme vom standardmäßigen Arbeitszeitprofil hat. Falls das Arbeitskraftprofil die Tagesschicht ist und sich die Arbeitskraft einverstanden erklärt hat, eine Nachtschicht ohne Überstunden zu arbeiten, müssen der Teamleiter oder Supervisor der das standardmäßige Arbeitskraftprofil überschreiben, um die Arbeitszeit mit der Standardnachtrate und nicht als Überstunden zu berechnen. Die Berechnung zeigt einen Fehler an, wenn eine Abwesenheitserfassung fehlt. Er muss vor hinzugefügt werden, bevor die Berechnung abgeschlossen werden kann.

## <a name="approving-registrations"></a>Genehmigen von Erfassungen
So wie Sie einer Arbeitskraft für Zeiterfassung eine Berechnungsgruppe zuweisen müssen Sie auch eine Genehmigungsgruppe zuweisen. Die Gruppe ist üblicherweise für ein bestimmtes Team, eine Schicht oder eine Arbeitsgruppe spezifisch. Sie müssen die Zeiterfassungen genehmigen, die ordnungsgemäß berechnet wurden (alle Berechnung wurden ohne Fehler durchgeführt), bevor Lohnelement generiert werden können, die danach zu einem Lohnsystem übertragen werden können. Der Lohnverwalter führt normalerweise die Genehmigung von Erfassungen durch. Vor der Genehmigung ist er in der Lage:
-   Lohnvereinbarung für bestimmte Arbeitskräfte zu überschreiben.
-   Manuelle Zulagen hinzuzufügen.
-   Zusätzliche Informationen über den Grund für Abwesenheitserfassungen einzugeben.

| **Hinweis**                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wenn für bestimmte Arbeitskräfte Überstunden berechnet wurden, können diese Überstunden bestimmten Einzelvorgängen im Verlauf eines Tages zugeordnet werden. Dies ist relevant, wenn Einzelvorgangskosten auf Basis des Lohns von Arbeitskräften berechnet werden. |

## <a name="approving-registrations-using-workflow"></a>Genehmigen von Erfassungen mithilfe des Workflows
Sie können einen Workflowgenehmigungsprozess einrichten, mit dem Erfassungen, die den im Workflow festgelegten Regeln entsprechen, automatisch genehmigt werden. So müssen nur Abweichungen manuell bearbeitet werden. Bei Verwendung der Workflowgenehmigung sendet der Teamleiter oder Supervisor die berechneten Erfassungen zur Genehmigung. Der Workflowprozess generiert die entsprechenden Genehmigungen und Aufgaben und weist sie den jeweiligen Benutzern und Rollen entsprechend des Workflows zu. Es gibt zwei Workflowgenehmigungen für Zeit und Anwesenheit.

| Workflow                                  | Verwendungszweck                                                                                                   | Registrierungstyp                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zeit und Anwesenheitstage gesamt            | Der Workflow prüft Erfassungen z. B. gegen die erwarteten Anzahl von Arbeitsstunden für den Tag. |                                                                                                                                                                                                                                                       |
| Zeit und Anwesenheit-Journalerfassung. | Im Workflow wird jeder Erfassungstyp mit dem Datum der Erfassung abgeglichen.                           | Zeit und Anwesenheit • Einstempeln • Ausstempeln • Abwesenheit • Pause • Wechselcode • Projekt • Projektaktivität • Produktionseinzelvorgänge der indirekten Aktivität • Warten davor • Einstellungen • Prozess • Überlappen • Transport • Warten danach • Assistenten starten • Assistenten stoppen |

 

## <a name="transferring-approved-registrations"></a>Genehmigte Erfassungen übertragen
Nach dem Genehmigen der Erfassungen können Sie sie an einen periodischen Lohneinzelvorgang übertragen. Eine übertragene Erfassung wird für die Aktivität oder den Einzelvorgang gebucht, auf die sie sich bezieht, z. B. einen Produktionsauftrag oder ein Projekt. Es werden anhand der Erfassungen Lohnabrechnungsbuchungen für jede Arbeitskraft generiert.  

## <a name="reversing-transferred-registrations"></a>Stornieren von übertragenen Erfassungen
Das Stornieren von Erfassungen (das Zurücksetzen) kann erfolgen, bis der Zahlungstransfer für die Lohnperiode ausgeführt wurde. Das bedeutet, dass die Lohndaten in eine externe Datei übertragen wurden. Bei einem Storno werden alle Erfassungen widerrufen, und alle Buchungen, die für Produktionsaufträge oder Projekte erfolgt sind, werden ausgeglichen und damit neutralisiert.

| **Hinweis**                                                 |
|----------------------------------------------------------|
| Die externe Datei kann in ein Lohnbuchhaltungssystem importiert werden. |

## <a name="registrations-in-electronic-timecards"></a>Erfassungen in elektronischen Zeitkarten
Arbeitskräfte mit Arbeitsaufgaben, die kein direktes Feedback erfordern (z. B. bei Produktionseinzelvorgängen), die an Projektaktivitäten arbeiten, können eine elektronische Zeitkarte nutzen. Elektronische Zeitkarten bieten die Flexibilität, Erfassungen zu jeder Zeit und bestmöglich entsprechend des täglichen Geschäftszeitplan (täglich, wöchentlich oder wenn eine Arbeitskraft wieder im Büro ist) einzugeben. Um elektronische Zeitkarten für diese Arbeitskräfte zu verwenden, müssen Sie "Zeitkarte verwenden" in den Arbeitskräftedetails festlegen. Elektronische Zeitkarten ermöglichen der Arbeitskraft die Erfassung von:

-   Datum
-   Registrierungstyp
-   Einzelvorgangsreferenzen wie dem Projekt, einem Produktionsauftrag oder einer indirekten Aktivität.
-   Einzelvorgang (Nummer)
-   Zeitaufwand
-   Projektgebühren
-   Projektartikeln





