---
title: Aufwendungsprüfer konfigurieren
description: In diesem Thema wird beschrieben, wie Sie Aufwendungsprüfer verwenden, um den Benutzer dynamisch auszuwählen, dem eine Workflowaufgabe, Genehmigung oder manuelle Entscheidung zugewiesen ist.
author: rachel-profitt
ms.date: 06/25/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2021-06-24
ms.openlocfilehash: ad980889247e0239ad743078cb013c1c5839f676
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070145"
---
# <a name="configure-expenditure-reviewers"></a>Aufwendungsprüfer konfigurieren
[!include[banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Sie können dynamische Aufwendungsprüfer einrichten, damit zu prüfende Aufwendungen basierend auf dem Benutzer weitergeleitet werden, der entweder einer Projektrolle oder der Finanzdimension zugewiesen ist, der die Aufwendung zugeschlagen wird. Im Workflowprozess wird die angegebene Projektrolle oder der Besitzer der Finanzdimension verwendet, um zu bestimmen, an wen die Aufwendungen weitergeleitet werden sollen.

Sie können eine oder mehrere Konfigurationen für Aufwendungsprüfer definieren und anschließend beim Erstellen eines Workflows eine Konfiguration auswählen. Sie können die Werte für Aufwendungsprüfer für jede juristische Person in der Organisation konfigurieren. Nachdem Sie die Konfigurationen für Aufwendungsprüfer definiert haben, weisen Sie die Konfiguration zu. Aufwendungsprüfer können Workflowaufgaben, Genehmigungen und manuellen Entscheidungen zugewiesen werden.

> [!NOTE]
> Obwohl Aufwendungsprüfer nicht obligatorisch sind, können sie die Konfiguration Ihres Workflows vereinfachen. Sie müssen beispielsweise nicht für jede Kostenstellendimension eine bedingte Entscheidung und dann ein weiteres Element erstellen, um die Genehmigung oder Aufgabe einem bestimmten Benutzer oder Benutzergruppen zuzuweisen. Stattdessen können Sie den Besitzer der Kostenstellendimension konfigurieren und einen Aufwendungsprüfer verwenden, um den richtigen Benutzer dynamisch auszuwählen. Auf diese Weise müssen Sie bei einer Änderung des Besitzes oder der Zuweisung von Kostenstellen nur das Feld **Besitzer** für die Finanzdimension.

## <a name="types-of-expenditure-reviewers"></a>Arten von Aufwendungsprüfern

Nicht alle Workflows unterstützen das Konzept der Aufwendungsprüfer. Standardmäßig können Sie Aufwendungsprüfer für Bestellanforderungen, Bestellungen, Kreditorenrechnungen und Aufwendungsberichte konfigurieren. Jeder dieser Workflowtypen erfordert, dass Sie die Aufwendungsprüfer auf einer separaten, für die Funktion und das Modul spezifischen Seite konfigurieren. Für jedes unterstützte Dokument können Aufwendungsprüfer entweder mit Workflows auf Kopfzeilenebene oder mit Workflows auf Zeilenebene verwendet werden.

Die folgende Tabelle zeigt, wo Sie einen Aufwendungsprüfer für jedes unterstützte Dokument konfigurieren.

| Dokument | Navigationspfad |
|----------|-----------------|
| Spesenabrechnungen | Ausgabenverwaltung \> Einrichten \> Richtlinien \> Aufwendungsprüfer |
| Bestellungen | Beschaffung \> Einrichten \> Richtlinien \> Aufwendungsprüfer für Bestellungen |
| Bestellanforderungen | Beschaffung \> Einrichten \> Richtlinien \> Aufwendungsprüfer für Bestellanforderungen |
| Kreditorenrechnungen | Kreditorenkonten \> Richtlinieneinstellung \> Aufwendungsprüfer Kreditorenrechnung |

## <a name="expenditure-reviewer-assignments"></a>Aufgaben des Aufwendungsprüfer

Für jeden Aufwendungsprüfer stehen zwei Arten von Zuweisungen zur Verfügung: *Projektverteilungen* und *Organisationsverteilungen*. Bei einer Projektverteilung können Sie zwischen Projektautoritäten und Finanzdimensionen wählen. Für eine Organisationsverteilung können Sie Finanzdimensionen auswählen.

Zu den Projektautoritäten gehören der Projektmanager, der Projektcontroller und der Projektverkaufsleiter. Sie definieren diese Autoritäten direkt in Ihrem Projekt, indem Sie eine Arbeitskraft in den entsprechenden Feldern auswählen.

Finanzdimensionen werden durch die Kontostrukturen in jeder juristischen Person gesteuert. Für jede juristische Person können Sie auswählen, welche Finanzdimensionen mit dem Aufwendungsprüfer verwendet werden. Die Dimensionen können entweder aus dem Projekt (in diesem Fall wählen Sie die Dimensionen in der Registerkarte **Projektverteilungen** aus) oder dem Dokument stammen (in diesem Fall wählen Sie die Abmessungen auf der Registerkarte **Organisationsverteilungen** aus). Sie können im Feld **Besitzer** auf der Seite **Finanzdimensionswerte** die Arbeitskraft für jede Finanzdimension auswählen.

## <a name="example-1-expenditure-reviewers-based-on-organization-distributions"></a>Beispiel 1: Aufwendungsprüfer basierend auf Organisationsverteilungen

Sie arbeiten für Contoso Appliances, und Ihr Unternehmen hat sechs Abteilungen und 10 Kalkulationsstellen. Als eine neue Bestellanforderung eingeht, muss sie zuerst vom Abteilungsleiter und dann vom Kostenstellenleiter genehmigt werden.

Für dieses Beispiel konfigurieren Sie zwei *Aufwendungsprüfer für Bestellanforderungen*:

- Geben Sie für den ersten Prüfer die Abteilung an und wählen Sie dann die Finanzdimension der **Abteilung** auf der Registerkarte **Organisationsverteilungen** aus. 
- Geben Sie für den zweiten Prüfer die Kostenstelle an und wählen Sie dann die Finanzdimension der **Kostenstelle** auf der Registerkarte **Organisationsverteilungen** aus.

Wenn Sie den Workflow konfigurieren, legen Sie zwei Genehmigungsschritte an. Der erste ist für die Abteilung und der zweite für die Kostenstelle. Für jedes Genehmigungselement wählen Sie **Teilnehmer** im Feld **Zuweisungstyp** der Registerkarte **Rollenbasiert** aus, wählen Sie **Aufwendungsteilnehmer** im Feld **Teilnehmertyp** und dann den entsprechenden Teilnehmer im Feld **Teilnehmer** aus.

Beim Anlegen der Bestellanforderung werden den Positionen der Bestellanforderung die Finanzdimensionen der Abteilung und Kostenstelle zugeordnet. Beim Absenden des Workflows wertet das System zunächst die Abteilung auf der Bestellanforderung aus und ordnet das Genehmigungselement dem Benutzer zu, der mit der von Ihnen für die Abteilung ausgewählten Arbeitskraft verknüpft ist. Nach Erledigung des ersten Genehmigungsschritts wertet das System den zweiten Genehmigungsschritt aus und ordnet das zweite Genehmigungselement dem Benutzer zu, der mit der von Ihnen für die Kostenstelle ausgewählten Arbeitskraft verknüpft ist.

## <a name="example-2-expenditure-reviewers-based-on-project-distributions"></a>Beispiel 2: Aufwendungsprüfer basierend auf Projektverteilungen

Sie arbeiten in der Abteilung für Dienstleistungen von Contoso Appliances. Die Organisation verlangt, dass der Projektmanager für jede Bestellung die Ausgabe genehmigen muss. Außerdem muss der Kostenstellenleiter des Projekts es genehmigen. Die Genehmigungen können gleichzeitig erfolgen. In jedem Fall müssen beide Benutzer die Bestellung genehmigen, bevor der Workflow fortgesetzt werden kann.

Für dieses Beispiel erstellen Sie einen *Aufwendungsprüfer für Bestellungen* namens **PM und Kostenstelle**. Sie wählen das Kontrollkästchen **Projektmanager** aus und setzen Sie die Option **Kostenstellendimension** auf **Ja** in der Registerkarte **Projektverteilungen** der Seite **Aufwendungsprüfer für Bestellungen**. Im Rahmen der Konfiguration müssen Sie sicherstellen, dass das Feld **Projektmanager** für alle Projekte festgelegt ist und dass für alle Kostenstellen auf der Seite **Finanzdimensionswerte** ein Besitzer festgelegt ist.

Wenn Sie den Workflow konfigurieren, brauchen Sie ein Genehmigungselement. Wählen Sie **Teilnehmer** im Feld **Zuweisungstyp** aus. Wählen Sie dann in der Registerkarte **Rollenbasiert** **Aufwendungsbeteiligte** im Feld **Teilnehmertyp** und dann den Projektmanager und die Kostenstelle im Feld **Teilnehmer** aus. Um sicherzustellen, dass der Workflow nicht fortgesetzt werden kann, bevor nicht sowohl der Projektmanager als auch der Kostenstellenbesitzer den Workflow genehmigt haben, legen Sie das Feld **Vollendungsrichtlinie** auf **Alle Genehmiger** fest.

Beim Anlegen der Bestellung muss das Feld **Projekt** angegeben werden. Wenn Sie nicht für alle Ihre Bestellungen ein Projekt benötigen, sollten Sie Ihrem Workflow eine bedingte Entscheidung hinzufügen, um vor Ausführung des Genehmigungsschritts nach einem Projekt zu suchen. Das System wertet dann das für die Bestellung angegebene Projekt aus und ordnet das Genehmigungselement dem Benutzer zu, der mit der Arbeitskraft im Feld **Projektmanager** verknüpft ist. Außerdem erstellt das System eine Aufgabe und weist sie dem Benutzer zu, der mit der Arbeitskraft verknüpft ist, die Sie im Feld **Besitzer** für die Kostenstelle aus dem Projekt auswählen. Beachten Sie, dass in diesem Beispiel die Kostenstelle des Projekts verwendet wird, nicht die Kostenstelle der Bestellung.

## <a name="set-up-expenditure-reviewers"></a>Aufwendungsprüfer einrichten

Dieses Beispiel zeigt, wie Sie einen Aufwendungsprüfer für Bestellanforderungen konfigurieren. Um andere Arten von Aufwendungsprüfern zu konfigurieren, ersetzen Sie den Navigationspfad in Schritt 1 durch den entsprechenden Pfad aus der Tabelle im Abschnitt [Arten von Aufwendungsprüfern](configure-expenditure-reviewers.md#types-of-expenditure-reviewers) weiter oben in diesem Thema.

1. Gehen Sie zu **Beschaffung \> Einrichten \> Richtlinien \> Aufwendungsprüfer für Bestellanforderungen**.
2. Wählen Sie auf der Seite **Aufwendungsprüfer für Bestellanforderungen** **Neu** aus.
3. Geben Sie im Feld **Name** einen Namen für die Konfiguration des Aufwendungsprüfers ein, z. B. **Kostenstelle**.
4. Wählen Sie im Inforegister **Aufwendungsprüfer nach juristischer Person** die zu konfigurierende juristische Person aus.
5. Aktivieren Sie für eine Projektverteilung das Kontrollkästchen für jede Projektautorität und wählen Sie für jede Finanzdimension, die Sie aktivieren möchten, **Ja** aus. 
6. Wählen Sie für eine Organisationsverteilung in der Registerkarte **Organisationsverteilungen** für jede Finanzdimension, die Sie aktivieren möchten, **Ja** aus.
7. Wiederholen Sie die Schritte 4 bis 6 für jede weitere juristische Person.

## <a name="assign-owners-to-financial-dimensions"></a>Finanzdimensionen Besitzer zuweisen

Um einer Finanzdimension Besitzer zuzuweisen, gehen Sie folgendermaßen vor.

1. Gehen Sie zu **Hauptbuch \> Kontenplan \> Dimensionen \> Finanzdimensionen**.
2. Wählen Sie in der Liste die Finanzdimension aus, der Sie Besitzer zuweisen möchten.
3. Wählen Sie **Dimensionswerte** aus.
4. Wählen Sie **Bearbeiten** aus, um die Dimensionswerte zu ändern.
5. Wählen Sie in der Liste die Dimensionswerte aus, der Sie einen Besitzer zuweisen möchten.
6. Wählen Sie im Feld **Besitzer** die Arbeitskraft aus, der der Dimensionswert zugewiesen werden soll.

## <a name="configure-project-distributions"></a>Projektverteilungen konfigurieren

Gehen Sie folgendermaßen vor, um einem Projekt Projektautoritäten zuzuweisen.

1. Wechseln Sie zu **Projektverwaltung und -verrechnung \> Projekte \> Alle Projekte**.
2. Wählen Sie das Projekt aus, dem Sie Autoritäten zuweisen möchten.
3. Wählen Sie **Bearbeiten** aus, um Änderungen an dem Projekt vorzunehmen.
4. Wählen Sie im Inforegister **Allgemein** im Abschnitt **Verantwortlich** wie erforderlich eine Arbeitskraft für die Felder **Verkaufsleiter**, **Projektmanager** und **Projektcontroller** aus.
5. Wählen Sie im Inforegister **Finanzdimensionen** die erforderlichen Finanzdimensionen für Ihr Projekt aus.

## <a name="assign-expenditure-reviewers-to-a-workflow-task"></a>Aufwendungsprüfer einer Workflowaufgabe zuweisen

In diesem Beispiel wird gezeigt, wie Sie einen Bestellanforderungsworkflow so konfigurieren, dass er einen Aufwendungsprüfer für Bestellanforderungen verwendet. Um andere Arten von Workflows zu konfigurieren, finden Sie die Workflowseite, die Sie in Schritt 1 öffnen müssen, möglicherweise im Modul **Ausgabenverwaltung** oder **Kreditorenkonten** anstatt im Modul **Beschaffung**.

Um Aufwendungsprüfer für Bestellanforderungen einer Workflowaufgabe zuzuweisen, gehen Sie wie folgt vor:

1. Gehen Sie zu **Beschaffung und Beschaffung \> Einrichten \> Beschaffungs- und Beschaffungsworkflows**.
2. Tippen oder klicken Sie doppelt auf einen vorhandenen Workflow oder erstellen Sie einen neuen Workflow.
3. Wählen Sie im Workflow-Editor im Bereich **Workflow** die Aufgabe aus, der die Konfiguration des Aufwendungsprüfers zugewiesen werden soll. Wählen Sie dann im **Aktivitätsbereich** in der Gruppe **Anzeigen** **Eigenschaften** aus.
4. Wählen Sie im linken Bereich der Seite **Eigenschaften** **Zuweisung** aus.
5. Auf der Registerkarte **Zuweisungstyp** wählen Sie **Teilnehmer**.
6. Wählen Sie auf der Registerkarte **Rollenbasiert** im Feld **Teilnehmertyp** **Aufwendungsteilnehmer** aus. Wählen Sie dann im Feld **Teilnehmer** die Konfiguration für Aufwendungsprüfer aus, die Sie für die Workflowaufgabe verwenden möchten.
