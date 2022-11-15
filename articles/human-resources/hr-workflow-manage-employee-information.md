---
title: Mitarbeiterinformationen mittels Workflows verwalten
description: In diesem Artikel wird erläutert, wie die Sie Workflows verwenden können, um Mitarbeiterdaten zu verwalten.
author: twheeloc
ms.date: 11/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dbbbb0ee807cb65fa4f4f9a29cc4a2b6b045b08c
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750733"
---
# <a name="use-workflows-to-manage-employee-information"></a>Mitarbeiterinformationen mittels Workflows verwalten

[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird erläutert, wie die Sie Workflowfunktion für die Personalverwaltung verwenden können, um Mitarbeiterdaten zu verwalten. So können Sie beispielsweise einen Workflow einer Position zuordnen und einen Genehmigungsworkflow konfigurieren, der gestartet wird, wenn Mitarbeiter Ihren Datensatz ändern.

Die Workflowfunktion für die Personalverwaltung beinhaltet zahlreiche Workflows zur Verwaltung von Personalverwaltungsaktivitäten. Darüber hinaus stehen zahlreiche Optionen zur Verfügung. So können Sie bestimmte Workflows ändern und einer Berichterstellungshierarchie zuordnen. Workflows sind verfügbar, um die Verwaltung von Änderungen an mehreren Typen der Mitarbeiterdaten zu unterstützten. Sie können einen Workflow einer Position zuordnen. Wenn Mitarbeiter dann ihren Datensatz ändern, wird ein Workflow gestartet, der eine Genehmigung erfordert, bevor die neuen Informationen gespeichert werden. Workflows sind für die folgenden Informationsarten vordefiniert, damit Sie Änderungen effizient verwalten können und die Daten Ihres Mitarbeiters immer korrekt sind.

-   Identifikationsnummern
-   Kurse
-   Ausbildung
-   Bild
-   Ausgeliehene Artikel
-   Berufserfahrung
-   Projekterfahrung
-   Qualifikationen
-   Vertrauensposition
-   Personalverwaltungsaktivitäten
-   Kursregistrierung

Wenn Mitarbeiter eingestellt oder übertragen werden oder das Beschäftigungsverhältnis beendet wird, kann der Workflow einen Prüfprozess enthalten. Auf diese Weise kann ein Dokument überarbeitet oder die Bedingungen für eine Aktivität als Teil des Workflows definiert werden. Nach Abschluss des Prüfprozesses wird das Dokument oder die Aktivität abgeschlossen. Der Workflow wird dann zum Schritt der abschließenden Genehmigung verschoben.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Zuordnen eines Workflows zu einer Positionshierarchie

Sie können einen Workflow einer beliebigen Positionshierarchie zuordnen, die Sie konfigurieren. Für das Workflow-Routing werden zwei Hierarchietypen verwendet: **Verwaltbar** und **Konfigurierbar**.

- Eine **verwaltbare** Hierarchie stellt die Berichtsstruktur des Unternehmens oder der Organisation dar. Weitere Informationen zu diesem Hierarchietyp finden Sie unter [Berichtet an Position](hr-personnel-positions.md#reports-to-position).
- Eine **konfigurierbar** Hierarchie stellt eine Matrix oder benutzerdefinierte Hierarchie dar. Weitere Informationen zu diesem Hierarchietyp finden Sie unter [Beziehungen](hr-personnel-positions.md#relationships).

### <a name="managerial-hierarchy-example"></a>Beispiel für verwaltbare Hierarchie

Sie können einen Workflow so konfigurieren, dass, wenn ein Mitarbeiter eine Kaufanfrage für einen neuen Computer sendet, die Anfrage an den Vorgesetzten des Mitarbeiters und den Vorgesetzten auf Skip-Ebene weitergeleitet wird. Legen Sie beim Konfigurieren des Workflow-Schritts das Feld **Zuweisungstyp** auf **Hierarchie** fest. Die **Hierarchietyp** Registerkarte wird dann verfügbar. Wählen Sie für dieses Beispiel die Hierarchie **Verwaltbar** aus.

### <a name="configurable-hierarchy-example"></a>Beispiel für konfigurierbare Hierarchie

Wird eine Position einer Matrixberichterstellungshierarchie zugeordnet, können Sie einen Workflow konfigurieren, der Ausgaben für ein bestimmtes Projekt an den Projektleiter weiterleitet und nicht an den Vorgesetzten des Mitarbeiters. Stellen Sie in diesem Fall das Feld **Zuweisungstyp** auf **Hierarchie**. Wählen Sie dann unter der Registerkarte **Hierarchietyp** die Option **Konfigurierbare** Hierarchie aus. Nachdem der Workflow eingerichtet ist, wählen Sie die **Assoziieren** Hierarchie auf der Seite **Workflow einrichten** aus, um die Hierarchie auszuwählen, die für das Workflow-Routing verwendet werden soll.

> [!IMPORTANT]
> Wenn ein Dokument, eine Transaktion oder ein Stammdatensatz zur Workflow-Genehmigung eingereicht wird, wird die primäre Position des Einreichers verwendet, um zu bestimmen, an wen das Dokument als nächstes weitergeleitet werden soll.

### <a name="hierarchy-setting-in-workflow-parameters"></a>Hierarchieeinstellung in Workflow-Parametern

1. Auf der **Workflow-Parameter** Seite, gehen Sie zu **Hierarchie-Routing**.
2. Standardmäßig ist die Option **Positionshierarchie verwenden** auf **Nein** festgelegt. In diesem Fall verwendet der Workflow die primäre Position der Arbeitskraft, wenn er durch die Hierarchie navigiert. Stellen Sie die Option auf **Ja** ein, damit der Workflow das übergeordnete Element der Position verwendet, wenn er in der Hierarchie navigiert.

### <a name="additional-example"></a>Zusätzliches Beispiel 

Mitarbeiterin Grace Sturman hat zwei Positionen: Beraterin und Trainerin. Graces Hauptposition ist Trainer. Wenn sie nicht gerade neue Mitarbeiter einarbeitet, steht sie beratend zur Verfügung. Durch ihre primäre Position berichtet Grace an Claire, die Leiterin der Personalabteilung. Claire erstattet Charlie Bericht. Für ihre Beraterposition hat Grace je nach Projekt mehrere gepunktete Beziehungen.

Das Unternehmen von Grace erstellt Workflow-Routing-Regeln, die auf einer **Konfigurierbaren** Hierarchie (Matrix-/projektbasierte Hierarchien) basieren. Diese Hierarchie verwendet die Beraterposition von Grace. Wenn die **Verwenden Sie die Positionshierarchie** Option auf **Nein** eingestellt ist, wenn ein Dokument zur Genehmigung an Grace weitergeleitet wird, prüft der Workflow ihre primäre Position (Trainer), um zu bestimmen, wohin das Dokument als nächstes weitergeleitet werden soll. In diesem Fall wird es zuerst an Claire und dann an Charlie weitergeleitet. Wenn die Option auf **Ja** eingestellt ist, und der Workflow eine **Konfigurierbare** Hierarchie verwendet, wird der Workflow die Beraterposition von Grace und die Berichtsbeziehung betrachten, um zu bestimmen, wohin das Dokument als nächstes weitergeleitet werden soll.

### <a name="configure-a-human-resources-workflow"></a>Konfigurieren eines Personalverwaltungsworkflows
Um einen grundlegenden Workflow zu konfigurieren, der startet, wenn Mitarbeiter Änderungen an ihrer persönlichen Kennung fordern, führen Sie die folgenden Schritte aus:

1.  Wählen Sie auf der Seite **Personalverwaltungsworkflows** **Neu** aus.
2.  Wählen Sie in der Liste der verfügbaren Workflows **Kennnummern** aus.
3.  Wählen Sie **Ausführen** aus, um den Workflowdesigner zu öffnen, und geben Sie Ihren Benutzernamen und Ihr Kennwort ein.
4.  Bewegen Sie das **Kennungsnummer genehmigen**-Element von der Liste der Workflowelemente in die Designercanvas.
5.  Verbinden Sie das Genehmigungselement mit **Start** und **Fertig stellen**.
6.  Tippen (oder klicken) Sie doppelt auf **Element genehmigen**, wählen und halten Sie (oder machen Sie einen Rechtsklick darauf) und wählen Sie dann **Eigenschaften** aus.
7.  Gehen Sie folgendermaßen vor, um Anweisungen für die Arbeitsaufgabe hinzuzufügen:

    1.  Wählen Sie **Zuweisung** und anschließend **Hierarchie** unter dem Zuweisungstyp aus.
    2.  Wählen Sie unter der **Hierarchie**-Auswahl die Option **Konfigurierbare Hierarchie** aus.
    3.  Fügen Sie eine Beendigungsbedingung hinzu, und schließen Sie die Seite.

8.  Schließen Sie alle zusätzlichen Anweisungen ab.
9.  Wählen Sie **Speichern und schließen**. Aktivieren Sie den neuen Workflow, wenn das Dialogfeld geöffnet wird, und wählen Sie **Als aktiv festlegen** aus.
10. Wechseln Sie zu **Personalverwaltung** &gt; **Positionen** &gt; **Hierarchietypen für die Position**.
11. Wählen Sie **Matrix** aus.
12. Fügen Sie den **Arbeitskraft-Kennungsnummer**-Workflow zur Liste hinzu.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Adressänderungen anzeigen und verwalten](hr-personnel-view-address-changes.md) 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
