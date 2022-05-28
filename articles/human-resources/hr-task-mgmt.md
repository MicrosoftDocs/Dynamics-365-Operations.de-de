---
title: Aufgabenverwaltung
description: In diesem Thema werden die in Microsoft Dynamics 365 Human Resources verfügbaren Aufgabenverwaltungsfunktionen erläutert.
author: twheeloc
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae453bd57217f272038decc7e40ed373f618ae03
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710220"
---
# <a name="task-management"></a>Aufgabenverwaltung

[!INCLUDE [PEAP](../includes/peap-1.md)]

Mit der Aufgabenverwaltung können Sie Aufgaben erstellen, die erledigt werden müssen, um Mitarbeiter einzustellen (onboard), zu kündigen (offboard) und zu versetzen (Transition). Das Aufgabenmanagement verwendet das Konzept von Checklisten. Eine Checkliste besteht aus einer Liste von Onboarding-, Offboarding- oder Übergangsaufgaben. Die Aufgabenverwaltung verwendet Checklisten, um Aufgaben zu gruppieren und sie einzelnen Personen oder Gruppen zuzuordnen. Die Checklistenfunktionalität für Onboarding, Offboarding und Übergänge ist ähnlich.

## <a name="checklist-overview"></a>Checklistenübersicht

Eine Checkliste ist eine Gruppe von Aufgaben. Checklisten ermöglichen eine flexible Gruppierung von Aufgaben und können wiederverwendet werden (z. B. bei der Einstellung zusätzlicher Mitarbeiter). Sie können beliebig viele Checklisten erstellen und dieselben Aufgaben mehreren Checklisten zuweisen.

### <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen, wie Checklisten im Onboarding-Prozess verwendet werden können. Da die Checklistenfunktionalität für Onboarding, Offboarding und Übergänge jedoch ähnlich ist, gelten die Informationen auch für die Offboarding- und Übergangsprozesse.

Als Teil des Onboarding-Prozesses können Human Resources (HR)-Experten Aufgaben erstellen, die den Onboarding-Fortschritt von neu eingestellten und neu eingestellten Mitarbeitern verfolgen. Da der Onboarding-Prozess je nach Position oder geografischem Standort des Mitarbeiters variieren kann, können Sie mehrere Onboarding-Checklisten erstellen, um unterschiedliche Einstellungssituationen zu berücksichtigen.

**Beispiel 1**

Jeder Mitarbeiter, der in den USA eingestellt wird, muss Aufgaben wie das Ausfüllen von Steuereinbehaltungsformularen erledigen. Aufgaben wie die Zuweisung eines Firmenwagens können jedoch nur für Führungskräfte auf Führungsebene gelten. In diesem Fall können zwei Onboarding-Checklisten erstellt werden: **Mitarbeiter mit Sitz in den USA** und **Nur Führungskräfte**. Wenn dann in den USA ein Manager auf mittlerer Ebene eingestellt wird, wird die **Mitarbeiter mit Sitz in den USA**-Checkliste ausgewählt. Wenn jedoch eine Führungskraft in den USA eingestellt wird, werden beide Checklisten ausgewählt, um sicherzustellen, dass alle erforderlichen Onboarding-Aufgaben abgeschlossen sind.

**Beispiel 2**

Ein Unternehmen hat sowohl Saisonkräfte als auch feste Vollzeitkräfte. Obwohl einige Aufgaben (wie die Überprüfung der Ankunftszeit des neuen Mitarbeiters) für beide Arten von Mitarbeitern gelten, gelten einige zusätzliche Aufgaben nur für reguläre Vollzeitbeschäftigte. In diesem Fall können Sie zwei Checklisten erstellen. Beide Checklisten enthalten die Aufgaben, die sowohl für Saison- als auch für reguläre Vollzeitbeschäftigte gelten, aber nur eine Checkliste enthält die Aufgaben, die für reguläre Vollzeitbeschäftigte spezifisch sind.

## <a name="task-management-workspace"></a>Arbeitsbereich für die Aufgabenverwaltung

Der Arbeitsbereich **Aufgabenverwaltung** listet alle Aufgaben auf, die Personen in den Onboarding-, Offboarding- und Übergangsprozessen zugewiesen wurden. Um die Aufgaben für einen Prozess anzuzeigen, wählen Sie die entsprechende Registerkarte in der oberen linken Ecke aus: **Onboarding**, **Offboarding** oder **Übergänge**. Standardmäßig haben nur HR-Experten Zugriff auf den Arbeitsbereich **Aufgabenverwaltung**.

Die **Onboarding**-Registerkarte enthält eine **Beginnt in Kürze**-Liste mit ankommenden Mitarbeitern und eine **Aktuellste Einstellungen**-Liste, die kürzlich eingestellte Mitarbeiter anzeigt. In beiden Listen können Sie nur einen Mitarbeiter auswählen. Wenn Sie einen Mitarbeiter auswählen, werden alle Aufgaben im Zusammenhang mit dem Onboarding dieses Mitarbeiters auf der rechten Seite der Seite angezeigt. Die **Onboarding**-Registerkarte enthält auch eine **Alle Aufgaben**-Liste, die alle Aufgaben für alle neu eingestellten oder neu eingestellten Mitarbeiter anzeigt. Schließlich enthält es eine Liste der überfälligen Aufgaben und eine Liste der Aufgaben, die dem aktuellen Benutzer zugewiesen sind.

Die **Offboarding**-Registerkarte enthält eine Liste der Mitarbeiter, die das Unternehmen verlassen und eine Liste der Mitarbeiter, die das Unternehmen bereits verlassen haben. In beiden Listen können Sie nur einen Mitarbeiter auswählen. Wenn Sie einen Mitarbeiter auswählen, werden alle Aufgaben im Zusammenhang mit dem Offboarding dieses Mitarbeiters angezeigt. Die **Offboarding**-Registerkarte enthält auch eine **Alle Aufgaben**-Liste, die alle Aufgaben für alle verlassenden oder entlassenen Mitarbeiter anzeigt. Schließlich enthält es eine Liste der überfälligen Aufgaben und eine Liste der Aufgaben, die dem aktuellen Benutzer zugewiesen sind.

Die **Übergänge**-Registerkarte enthält eine **Alle Aufgaben**-Liste, die alle Aufgaben für alle Mitarbeiter anzeigt, die die Position wechseln werden oder kürzlich die Position gewechselt haben. Es gibt auch eine Liste der überfälligen Aufgaben und eine Liste der Aufgaben, die dem aktuellen Benutzer zugewiesen sind.

Auf allen drei Registerkarten können Personalassistenten und -Manager die folgenden Aktivitäten ausführen:
- Eine Checkliste auf einen Mitarbeiter anwenden
- Den Status einer Aufgabe aktualisieren
- Eine Aufgabe neu zuweisen
- Das Fälligkeitsdatum einer Aufgabe aktualisieren

> [!NOTE]
> Standardmäßig zeigt die Registerkarte **Onboarding** Mitarbeiter an, die in den letzten sieben Tagen eingestellt wurden. Um diese Einstellung zu ändern, legen Sie auf der Seite **Personalverwaltungsparameter** auf der Registerkarte **Allgemein** einen Zeitrahmen für **Aktuellste Einstellungen** fest. Die Informationen im Abschnitt **Aktuellste Einstellungen** können als Tage, Monate oder Jahre angezeigt werden. Um zum Beispiel die Liste der Mitarbeiter anzuzeigen, die in den letzten 14 Tagen eingestellt wurden, stellen Sie das Feld **Zeitraum** auf **14** und **Einheit** auf **Tage** ein.
> Auf der **Personalverwaltungsparameter**-Seite können Sie auch den Datumsbereich für die Listen der ausscheidenden und ausgeschiedenen Mitarbeiter aktualisieren, die auf der Registerkarte **Offboarding** angezeigt werden. Diese Einstellungen gelten auch für den Arbeitsbereich **Personalverwaltung**.

## <a name="setting-up-tasks"></a>Einrichten von Aufgaben

Sie können Aufgaben einzeln erstellen und diese dann in mehreren Checklisten wiederverwenden. Um eine Aufgabe zu erstellen, wählen Sie auf der **Onboarding-Setup**-Seite auf der **Aufgaben**-Registerkarte **Neu** aus.

Alternativ können Sie Aufgaben direkt zu einer Checkliste hinzufügen. Um eine Aufgabe zu einer Checkliste hinzuzufügen, erstellen Sie auf der Seite **Onboarding-Setup** auf der **Checkliste**-Registerkarte entweder eine neue Checkliste, um die Aufgabe hinzuzufügen, oder fügen Sie die Aufgabe zu einer vorhandenen Checkliste hinzu.

> [!NOTE]
> Wenn Sie eine Aufgabe direkt zu einer Checkliste hinzufügen, können Sie sie nicht in anderen Checklisten wiederverwenden.

In der folgenden Tabelle werden die Felder beschrieben, die verfügbar sind, wenn Sie eine Aufgabe mit einer der Methoden erstellen.

| Feld           | Description |
|-----------------|-------------|
| Aufgabe            | Geben Sie den Namen der Aufgabe ein. |
| Description     | Geben Sie eine Beschreibung der Aufgabe ein. |
| Optional        | Geben Sie an, ob die Aufgabe optional ist und nur zu Informationszwecken dient. |
| Aufgabenlink       | Geben Sie die URL einer externen Webseite oder einer bestimmten Seite in der App ein, auf der der Benutzer die Aufgabe ausführen soll. Weitere Informationen finden Sie im Abschnitt [Aufgabenlinks](#task-links). |
| Zuweisungstyp | Aufgaben können einer bestimmten Arbeitskraft, Planstelle oder Planstellengruppe, dem Vorgesetzten des betroffenen Mitarbeiters (d. h. dem Mitarbeiter, der am Onboarding-, Offboarding- oder Übergangsprozess teilnimmt) oder dem betroffenen Mitarbeiter zugewiesen werden. Wählen Sie den Zuweisungstyp aus. Weitere Informationen finden Sie im Abschnitt [Zuweisungstyp](#assignment-types). |
| Zugewiesen zu     | Wählen Sie die spezifische Arbeitskraft, Position oder Gruppe von Positionen aus, der die Aufgabe zugewiesen werden soll. |
| Ansprechpartner  | Geben Sie die Person an, die bei Fragen zur Aufgabe kontaktiert werden soll. |
| Fälligkeitsdatum-/Uhrzeit-Offset | Geben Sie die Anzahl der Tage vor oder nach dem Onboarding-, Beendigungs- oder Übergangsdatum an, an dem die Aufgabe fällig ist. Weitere Informationen finden Sie im Abschnitt [Fälligkeitsdatum, das sich auf das Zieldatum bezieht](#task-due-dates-and-the-due-date-offset-field). |
| Anweisungen    | Geben Sie Anweisungen zum Ausführen der Aufgabe ein. Weitere Informationen finden Sie im Abshnitt [Anweisungen](#instructions). |

### <a name="task-links"></a>Aufgabenlinks

Ein Aufgabenlink stellt einen Link zu einer externen Webseite oder einer Seite in der Dynamics 365-App bereit. Sie können einen Aufgabenlink angeben, wenn die Person, der eine Aufgabe zugewiesen ist, zu einer bestimmten Webseite oder einer bestimmten Seite in der Dynamics 365-App gehen soll, um diese Aufgabe abzuschließen. Wenn Sie einen Aufgabenlink erstellen, können Sie eine der folgenden Optionen auswählen:

- **Menüelement** – Wenn Sie diese Option auswählen, wird eine Liste aller Seiten in der Dynamics 365-App angezeigt. Wählen Sie eine Seite in der Liste aus.
- **URL** – Wenn Sie diese Option auswählen, geben Sie die URL der Webseite ein, zu der die Person, die der Aufgabe zugewiesen ist, gehen soll. Die angegebene Seite kann eine Seite sein, die nicht Teil der Dynamics 365-App ist.
- **Mitarbeiterdetails** – Wenn Sie diese Option auswählen, wählen Sie eine der folgenden Optionen:

    - **Self-Service-Aktionen für Mitarbeiter** – Diese Option zeigt eine Liste der Seiten an, die in **Mitarbeiter-Self-Service** verfügbar sind. Verwenden Sie es, wenn die dem Onboarding-Mitarbeiter zugewiesene Aufgabe in **Mitarbeiter-Self-Service** abgeschlossen werden muss. Wenn Sie beispielsweise möchten, dass der Mitarbeiter seine persönlichen Kontaktdaten eingibt, wählen Sie **Self-Service-Aktionen für Mitarbeiter** und dann **Persönliche Daten&gt;Persönliche Informationen** aus.
    - **Maßnahmen zur Mitarbeiterverwaltung** – Diese Option zeigt eine Liste von Seiten an, die sich auf den Datensatz des Mitarbeiters beziehen, aber für den Mitarbeiter nicht zugänglich sind. Wenn Sie beispielsweise möchten, dass der Aufgabeneigentümer Informationen eingibt, die spezifisch für einen aufgenommenen Mitarbeiter sind, z. B. Vergütungsinformationen, wählen Sie **Maßnahmen zur Mitarbeiterverwaltung** und dann **Vergütung&gt;Feste Vergütung** aus.

### <a name="assignment-types"></a>Zuweisungstypen

Wenn ein Mitarbeiter eingestellt, gekündigt oder versetzt wird, können eine oder mehrere Checklisten ausgewählt werden. Nachdem eine Checkliste ausgewählt wurde und der Einstellungs-, Kündigungs- oder Versetzungsprozess abgeschlossen ist, werden Aufgaben erstellt und den Benutzern zugewiesen, um den Fortschritt zu verfolgen.

Wenn eine Aufgabe erstellt wird, wird sie einem bestimmten Benutzer zugewiesen. Welchem Benutzer eine Aufgabe zugewiesen wird, hängt von dem für diese Aufgabe ausgewählten Zuweisungstyp ab. Die folgenden Werte stehen im Feld **Zuweisungstyp** zur Verfügung:

- **Arbeiter** – Weisen Sie die Aufgabe einer bestimmten Arbeitskraft zu. Nachdem Sie diesen Wert ausgewählt haben, wählen Sie den Arbeiter im **Zugewiesen zu**-Bereich aus.
- **Position** – Weisen Sie die Aufgabe einer bestimmten Position zu. Nachdem Sie diesen Wert ausgewählt haben, wählen Sie die Position im **Zugewiesen zu**-Bereich aus.

    Ein IT-Ingenieur ist beispielsweise immer dafür verantwortlich, einen Laptop für einen neuen Mitarbeiter vorzubereiten. Wenn Sie in diesem Fall die Laptop-Konfigurationsaufgabe erstellen, wählen Sie die **Position** für den Zuweisungstyp aus, und wählen Sie dann **IT-Ingenieur** als Position aus. Wenn dann ein Mitarbeiter eingestellt und die Checkliste zugewiesen wird, wird die Laptop-Konfigurationsaufgabe dem Mitarbeiter zugewiesen, der sich zum Zeitpunkt der Einstellungsaktion auf der IT-Ingenieurposition befindet.

- **Gruppe** – Ordnen Sie die Aufgabe einer Gruppe von Planstellen (Zuordnungsgruppe) zu. Nachdem Sie diesen Wert ausgewählt haben, wählen Sie die Gruppe im **Zugewiesen zu**-Bereich aus. Weitere Informationen finden Sie im Abschnitt [Einrichten von Zuweisungsgruppen (optional)](#setting-up-assignment-groups-optional).
- **Manager** – Weisen Sie die Aufgabe dem Vorgesetzten des Mitarbeiters zu, der eingestellt, gekündigt oder versetzt wird.

    > [!IMPORTANT]
    > Wenn eine Checkliste angewendet wird und dem eingestellten, gekündigten oder versetzten Mitarbeiter derzeit keine Position zugewiesen ist, kann der Vorgesetzte nicht bestimmt werden. In diesem Fall wird die Aufgabe dem Checklistenbesitzer zugewiesen. Weitere Informationen finden Sie im Abschnitt [Einrichten von Checklisten](#setting-up-checklists).

- **Mitarbeiter** – Weisen Sie den Mitarbeiter zu, der eingestellt, gekündigt oder versetzt wird.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Fälligkeitsdaten für Aufgaben und das Feld Fälligkeitsdatumsversatz

Die Fälligkeitsdaten von Aufgaben basieren auf dem Beschäftigungsbeginn-, Beendigungs- oder Übergangsdatum. Einige Aufgaben müssen vor dem Startdatum eines Mitarbeiters abgeschlossen sein, während andere Aufgaben danach abgeschlossen werden können. Wenn Sie eine Aufgabe definieren, geben Sie ein **Fälligkeitsdatum-/Uhrzeit-Offset** relativ zum Beschäftigungsbeginn-, Beendigungs- oder Übergangsdatum ein. Ein IT-Ingenieur muss beispielsweise zwei Tage vor dem Startdatum dieses Mitarbeiters einen Laptop für einen neuen Mitarbeiter vorbereiten. Legen Sie in diesem Fall beim Erstellen der Laptop-Konfigurationsaufgabe das **Fälligkeitsdatum-/Uhrzeit-Offset**-Feld auf **-2** fest. Wenn das Startdatum eines Mitarbeiters dann der 5. Mai ist, wird die Aufgabe am 3. Mai fällig.

> [!NOTE]
> Fälligkeitsdatum kann auch geändert werden, nachdem die Aufgabe erstellt wurde.

Die Fälligkeitsdaten werden basierend auf dem Kalender berechnet, der der Checkliste zugeordnet ist. Weitere Informationen finden Sie im Abschnitt [Einrichten von Checklisten](#setting-up-checklists).

### <a name="instructions"></a>Anweisungen

Komplexe Aufgaben erfordern möglicherweise mehrere Schritte, oder benötigen das Ausführen von Aufgaben, um die zusätzlichen Informationen bereitzustellen. Im Feld **Anweisungen** können Sie Anweisungen oder zusätzliche Informationen angeben, um der Person zu helfen, die mit dem Abschluss der Aufgabe betraut wurde.

## <a name="setting-up-checklists"></a>Einrichten von Checklisten

Eine Checkliste ist eine Gruppe von Aufgaben. Sie können beliebig viele Checklisten erstellen und dieselben Aufgaben mehreren Checklisten zuweisen. Wenn Sie eine Checkliste erstellen, geben Sie einen Besitzer und einen Kalender an.

Wenn das **Zuweisungstyp**-Feld für eine Aufgabe auf **Position**, **Manager** oder **Gruppe** festgelegt ist, aber aus dem Aufgabentyp keine konkrete Person abgeleitet werden kann, wird die Aufgabe dem Checklistenverantwortlichen zugewiesen. Hier sind einige Beispiele für Situationen, in denen dem Checklistenbesitzer Aufgaben zugewiesen werden:

- Einem Mitarbeiter, der eingestellt oder gekündigt wird, wird keine Position zugewiesen. Da der Mitarbeiter keine Positionszuordnung hat, kann sein Vorgesetzter nicht ermittelt werden.
- Das **Zuweisungstyp**-Feld ist auf **Position** gesetzt, aber der Planstelle ist zum Zeitpunkt der Aufgabenerstellung kein Mitarbeiter zugeordnet. Die Aufgabe **Laptop einrichten** ist beispielsweise der Positionsnummer 000876 (**Spezialist des technischen Hilfedienstes**) zugeordnet. Zum Zeitpunkt der Einstellung eines Mitarbeiters ist der Position 000876 kein Mitarbeiter zugeordnet. Daher wird eine Aufgabe für den Checklistenbesitzer erstellt.
- Das **Zuweisungstyp**-Feld ist auf **Gruppe** gesetzt, aber den Positionen in der Gruppe ist zum Zeitpunkt der Aufgabenerstellung kein Mitarbeiter zugeordnet.

Der für eine Checkliste angegebene Kalender wird verwendet, um das Fälligkeitsdatum von Aufgaben zu berechnen, die Teil dieser Checkliste sind. Arbeits- und arbeitsfreie Tage werden im Kalender-Setup definiert. Arbeitstage werden bei der Berechnung des Fälligkeitsdatums von Aufgaben berücksichtigt, arbeitsfreie Tage werden ausgeschlossen. Zu den arbeitsfreien Tagen zählen Wochenenden und Feiertage. 

Nachdem ein Kalender eingerichtet wurde, wird er mit einer Checklistenvorlage verknüpft. Auf diese Weise wird das Fälligkeitsdatum jeder Aufgabe in der Checkliste auf die gleiche Weise berechnet. Sie können mehrere Kalender einrichten, aber jeder Checkliste kann nur ein Kalender zugeordnet werden.

## <a name="setting-up-assignment-groups-optional"></a>Einrichten von Zuweisungsgruppen (optional)

Manchmal ist eine Gruppe von Einzelpersonen für eine Aufgabe verantwortlich. Beispielsweise könnte eine Gruppe von IT-Mitarbeitern dafür verantwortlich sein, Laptops für neue Mitarbeiter vorzubereiten.

Gehen Sie zum Einrichten einer Zuweisungsgruppe folgendermaßen vor.

1. Wählen Sie auf der Seite **Gruppenzuweisung** die Option **Neu** aus.
1. Geben Sie einen Namen ein (z. B. **IT-Laptop**) und eine Beschreibung für die Gruppe ein.
1. Wählen Sie **Speichern** aus.
1. Wählen Sie auf der Inforegisterkarte **Mitglieder** die Option **Hinzufügen**.
1. Im **Positionen**-Feld wählen Sie alle Stellen aus, die für die Aufgabe zuständig sind.

Nachdem eine Aufgabengruppe erstellt wurde, steht sie beim Erstellen einer Aufgabe zur Auswahl. Um eine bestimmte Gruppe für eine Aufgabe auszuwählen, müssen Sie **Gruppe** in **Zuiweisungstyp** auswählen. Die von Ihnen erstellte Gruppe steht dann zur Auswahl im **Zugewiesen zu**-Bereich.

> [!IMPORTANT]
> Wenn einer Gruppe eine Aufgabe zugewiesen ist, wird die Aufgabe als **Abgeschlossen** gekennzeichnet, wenn eine Person in der Gruppe sie vervollständigt. Aufgaben werden zum Zeitpunkt der Einstellung, Beendigung oder des Übergangs erstellt. Sie werden für die Benutzer erstellt, die den Positionen zugeordnet sind, die in der Gruppe enthalten sind.

## <a name="setting-up-task-groups-optional"></a>Einrichten von Aufgabengruppen (optional)

Ein Onboarding-, Offboarding- oder Übergangsprozess kann viele Aufgaben umfassen. Um die Zuordnung aller erforderlichen Aufgaben zu einer Checkliste zu erleichtern, können Sie optionale Aufgabengruppen erstellen, um verwandte Aufgaben zu kategorisieren. Beispielsweise müssen die Personal-, IT- und Gehaltsabrechnungsabteilungen jeweils spezifische Aufgaben erfüllen, um einen neuen Mitarbeiter einzustellen. Daher erstellen Sie die folgenden Aufgabengruppen: **HR**, **IT** und **Gehaltsabrechnung**. Wenn Sie dann eine Aufgabe erstellen, können Sie ihr eine dieser Aufgabengruppen zuordnen.

Wenn Sie einer Checkliste eine Aufgabe hinzufügen möchten, können Sie die Aufgabenliste nach der Aufgabengruppe filtern, der die gewünschte Aufgabe zugewiesen ist. Wenn Sie beispielsweise eine Checklistenvorlage erstellen, können Sie die Liste so filtern, dass nur die IT-Aufgaben, die der **IT**-Aufgabengruppe zugewiesen sind, angezeigt werden. Somit können Sie sicherstellen, dass nur die relevanten IT-Aufgaben ausgewählt werden.

## <a name="using-checklists"></a>Checklisten verwenden

Wenn eine Arbeitskraft eingestellt, gekündigt oder versetzt wird, können eine oder mehrere Checklisten ausgewählt werden. Fälligkeitstermine für Aufgaben und Arbeitskraftzuweisungen werden erstellt, nachdem der Einstellungs-, Kündigungs- oder Übergangsprozess abgeschlossen ist. Wenn Sie beispielsweise die Schaltflächen **Einstellen** oder **Einstellen und Details hinzufügen** auswählen, werden Aufgaben für Einzelpersonen erstellt, basierend auf dem Zuweisungstyp basieren.

Jeder Aufgabe wird ein Fälligkeitsdatum zugeordnet, indem der Fälligkeits-Offset vom Startdatum des Mitarbeiters addiert oder abgezogen wird. Weitere Informationen finden Sie im Abschnitt [Fälligkeitsdatum, das sich auf das Zieldatum bezieht](#task-due-dates-and-the-due-date-offset-field).

Wenn Sie Personalmaßnahmen verwenden, werden die Aufgaben erstellt, wenn die **Abgeschlossen**-Schaltfläche ausgewählt oder die Aktion genehmigt wird.

Im **Aufgabenverwaltung**-Arbeitsbereichs können Sie eine Checkliste auf einen Mitarbeiter anwenden, indem Sie den Mitarbeiter auf der einfachen Listenseite oder der Detailseite auswählen und dann **Checkliste anwenden** auswählen. Der Wert des **Zieltermin**-Felds wird verwendet, um das Fälligkeitsdatum der Aufgaben zu berechnen. Normalerweise sollte das Zieldatum mit dem Datum der Einstellung, Kündigung oder des Übergangs des Mitarbeiters übereinstimmen.

Sie können eine Checkliste auch auf einen Mitarbeiter anwenden, indem Sie dessen Seite **Arbeitskraft** öffnen und **Checklisten** im Menü auswählen.

## <a name="completing-tasks"></a>Aufgaben abschließen

Auf der Seite **Mitarbeiter-Self-Service** kann ein Mitarbeiter alle ihm zugewiesenen Aufgaben anzeigen. Für jede zugewiesene Aufgabe werden die Werte **Aufgabe**, **Beschreibung**, **Anweisungen** und **Kontaktperson** angezeigt. Darüber hinaus kann der Mitarbeiter für jede Aufgabe die zugehörige externe Webseite oder die zugehörige Seite in der Dynamics 365-App öffnen.

Aufgaben können auch auf dem Standard-Dashboard angezeigt werden. So zeigen Sie Aufgaben im Standard-Dashboard an:
1. Gehen Sie zu **Benutzeroptionen – Voreinstellungen – Aufgabenverwaltung** 
2. Legen Sie **Aufgaben im Standard-Dashboard anzeigen** auf **Ein** fest.  

>[!Note] 
>Die **Aufgabenverwaltung**-Funktion muss in **Funktionsverwaltung** aktiviert sein, damit die Option in **Benutzeroptionen** angezeigt wird.

Aufgaben können als **In Bearbeitung**, **Abgebrochen** oder **Abgeschlossen** markiert werden. Wenn einer Gruppe eine Aufgabe zugewiesen ist, wird die Aufgabe als **Abgeschlossen** gekennzeichnet, wenn eine Person in der Gruppe sie vervollständigt.

Aufgaben können auch neu zugewiesen werden.
