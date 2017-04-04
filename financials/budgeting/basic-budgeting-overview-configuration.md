---
title: "Budgetierungsüberblick"
description: "Fast jedes Unternehmen, das Finanzverhältnisfunktionen in Microsoft Dynamics 365 für Arbeitsgänge verwendet werden, müssen den Status erhalten, Berichte des Budgets durch Vergleich mit den Wirklichkeiten zu erstellen. In diesem Artikel wird beschrieben die Mindstausstattung, die erforderlich ist, um Budgets in Dynamics 365 für Arbeitsgänge erstellen oder er von einem Programm zum Laden von Drittanbietern."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a639e509cf6a3d2f1b850f27481d7b95546522b8
ms.openlocfilehash: b62e14f7c91692ae97bb332b38b0deeb328cc1bd
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-overview"></a>Budgetierungsüberblick

Fast jedes Unternehmen, das Finanzverhältnisfunktionen in Microsoft Dynamics 365 für Arbeitsgänge verwendet werden, müssen den Status erhalten, Berichte des Budgets durch Vergleich mit den Wirklichkeiten zu erstellen. In diesem Artikel wird beschrieben die Mindstausstattung, die erforderlich ist, um Budgets in Dynamics 365 für Arbeitsgänge erstellen oder er von einem Programm zum Laden von Drittanbietern.

<a name="overview"></a>Überblick
--------

Das genehmigte Budget für eine juristische Person wird in einem Dokument verwaltet, das als *Budgetregistereintrag* bekannt ist. Die Positionen in einem Budgetregistereintragsdokument wird als *budget Einträge enthalten account* und Finanzdimensionsinformationen, Datumsangaben und Beträge genehmigter Budgets. Das Budgetregistereintragsdokument wird mit grundlegenden und Abfragenseiten Finanzberichten integriert, in dem die tatsächlichen Beträge des Sachkontos zu den Budgetbeträgen verglichen werden. 

Es gibt mehrere Methoden für das Erstellen von Budgetregistereinträgen in Dynamics 365 für Arbeitsgänge:

-   Geben Sie die Dokumentinformationen auf der Seite **Budgeterfassungseinträge** manuell ein.
-   Verwenden Sie die Microsoft- Excelvorlage, die geöffnet können, indem Sie auf der Seite **in Excel öffnen** auf die Schaltfläche **Budgetregistereinträge** klicken.
-   Verwenden Sie die **Budgetkontoeinträge** Datenentität in der Datenverwaltung, um Budgetregistereinträge zu importieren. Sie können diese Methode anzuwenden zu aktivieren, und nehmen ** der Wechselkurs basiert ** ** Verarbeitungseinstellungen ** Parameter, wenn Sie zahlreiche Budgetkontoeinträge in das System importiert werden müssen.
-   Wenn das Unternehmen Planungsfunktionen plant, um Budgetdaten vorzubereiten, können Sie den periodischen Prozess**Budgetregistereintrag erstellen** verwenden.

Der Budgetregistereintrag wird als abgeschlossen, wenn die Budgetsalden aktualisiert wurden. ** Auf der Budgeterfassungseinträge ** Seite, um Aktualisierungsbudgetsalden ** ** für einen ausgewählten oder mehreren Einträgen den Budgetregistereintrag. Nachdem Sie die Budgetsalden aktualisiert haben, wird der Status des Budgetregistereintrags auf **Abgeschlossen** gesetzt. Ein abgeschlossener Budgetregistereintrag kann nicht erneut zum Bearbeiten geöffnet werden. Wenn die Budgetdaten angepasst werden müssen, müssen Sie einen neuen Budgetregistereintrag erstellen, anstatt die Daten im abgeschlossenen Budgetregistereintrag zu korrigieren.

## <a name="configuration"></a>Konfiguration
Wenn Sie die Budgetierung konfigurieren, beginnen Sie auf der Seite **Budgetierungsparameter**. Auf dieser Seite müssen Sie die Budgeterfassung, die Zahlenfolge für die Budgetregistereinträge und das Standardverhalten in den Arbeitsbereichen definieren.

Wenn es Richtlinien gibt, die die Genehmigung von Budgetregistereinträgen basierend auf dem Budgettyp regeln (beispielsweise Übertragungen oder Überarbeitungen), müssen Sie Budgetregistereintrags-Workflows auf der Seite **Budgetierungs-Workflows** erstellen. Sind Szenarien vorhanden, bei denen Übertragungen ohne Workflowgenehmigung zulässig sind, können Sie Budgetübertragungsregeln definieren, die diese Szenarien unterstützen. 

Wählen Sie auf der Seite **Budgetierungsdimensionen** Finanzdimensionen, die für die Budgetierung basierend auf den im Kontenplan verwendeten Dimensionen verwendet werden. Sie können für die Budgetierung alle Finanzdimensionen oder eine Auswahl davon auswählen.

Definieren Sie ein *budget Modell entspricht *that allen oder mehreren der Budgets. Sie können ein einziges Budgetmodell für alle Budgetregistereinträge verwenden. Alternativ können Sie separate Modelle erstellen, die auf dem Budgettyp, dem geografischen Standort oder einen beliebigen anderen Methode, mit der ein Budget klassifiziert werden kann, basiert. 

> [!NOTE] 
> Wenn die Budgetsteuerung verwendet wird, kann nur ein Budgetmodell mit einer bestimmten Zeitspanne für Budgetzyklus zugeordnet. 

Erstellen Sie *Budgetcodes *, die den Typ der zu erfassenden Budgettransaktionen und die damit im Zusammenhang stehende Workflows identifizieren. Budgetcodes können die folgende Budgettypen unterstützen:

-   Ursprüngliches Budget
-   Umlagerung
-   Überarbeitung
-   Belastung
-   Vorabbelastung
-   Vortragsbudget

Budgetcodes geben Ihnen einen Audit-Trail mit den im Verlauf des Budgetzyklus genehmigten Budgetänderungen. Wenn ein Workflow einem Budgetcode zugeordnet ist, wird der Workflow aktiviert für alle Budgetregistereinträge, die diesen Budgetcode verwenden, und Workflowschritte müssen ausgeführt werden, bevor dem Budgetregistereintrag ** die abgeschlossen ** Phase eingeben kann.  

Sie können *budget Übergangs-rules* optional auch einrichten. Wenn Sie folglich zu verwenden, aktivieren Sie ** verwenden Sie Regeln für Budgetübertragungen ** ** Budgetparameter ** auf der Seite aus. Wenn Budgetübertragungsregeln verwendet werden, wenn ein Benutzer ein Dokument mithilfe des Budgetcodes vom Typ **Übertragen** erstellt, werden Budgetsalden nicht aktualisiert, wenn die Budgetübertragungsregeln verletzt werden. Sie können beispielsweise Budgetübertragungsdokumente zulassen, wenn das Ausgabenbudget zwischen den Hauptkonten für die Vertriebs- und Marketingabteilung übertragen werden, kann jedoch verhindern, dass Budget von dieser Abteilung oder zu dieser übertragen wird, sofern keine Workflowgenehmigung für diesen Typ von Budgetkontoeinträgen gewährt wurde.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Verwenden der Arbeitsbereiche und Anfragenseiten, um des Budgets im Vergleich zum Istwert zu verfolgen
Der Budget-Manager kann den aktuellen Status eines Budgets im Arbeitsbereich **Sachkontobudgets und Planungen** überprüfen. Die Registerkarten **Ausgaben über Budget** und **Umsatzerlös unter Budget** geben einen raschen Überblick über die Finanzdimensionskombinationen, wenn Budgetziele nicht erfüllt werden oder sich dem Schwellenwert nähern. Sie können den Budgetschwellenwertprozentsatz und die Finanzdimensionssätze, die in diesen Registerkarten verwendet werden, personalisieren, indem Sie den **Meinen Arbeitsbereich konfigurieren** anklicken. Sie können auf **Einheiten-Manager** klicken, um die Arbeitskräfte anzuzeigen, die für bestimmte Finanzdimensionskombinationen, die auf diesen Registerkarten ausgewählt werden, verantwortlich sind. Wenn Sie beispielsweise sehen, dass das Ausgabenbudget der Betriebsabteilung den Budgetschwellenwert überschreitet, können Sie den Betriebsabteilungsmanager einfach auffinden, um das Problem zu diskutieren. 

> [!NOTE] 
> ** Der Abteilungsleiter ** Feld auf der Organisationseinheiten ** ** Seite abhängig, welche bestimmte Finanzdimensionskombinationen Manager unterstützen. Klicken Sie **Mehr** am unteren Rand der Registerkarte, um die Abfrageseite**Budget im Vergleich zum Istwert** zu öffnen, um weitere Details zu Budgetbeträge im Vergleich zu den aktuellen Beträgen zu erhalten. 

Auf der Abfrageseite **Istwert verglichen mit Budget** können Sie zu den Details des Budgets im Vergleich zu den Istwerten blättern. Wählen Sie eine Position auf der Abfrageseite aus und klicken Sie dann **Periodensaldi** an, um das Budget und die Istwerte im Finanzzeitraum anzusehen. Die Seite **Budgetkontoeinträge** enthält Drillthroughs zu den Details des Budgetbetrags im Budgetregistereintrag. Die Seite **Allgemeine Erfassungseinträge **öffnet die Sachkontobuchungen, die im berechneten Betrag **Istwerte** enthalten sind. 

Ein Unternehmen, das Budgetplanungsfunktionen verwendet, kann im Arbeitsbereich unter *Sachkontenbudget und Planung*. **Budgetplanung** verwenden.


