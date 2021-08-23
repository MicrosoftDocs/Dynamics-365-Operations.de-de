---
title: Fragebögen erstellen
description: In diesem Artikel wird der Prozess zum Erstellen eines Fragebogens beschrieben. Der erste Schritt ist das Entwerfen des Fragebogens. Wenn Sie einen Fragebogen entwerfen, schreiben Sie nicht nur Fragen und Antworten, Sie erstellen auch die Struktur, die es ermöglicht, Antworten zu erfassen und zu tabellieren.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: c2a8c156aa75b02b69da3ee70a1ee60ea9d73a8aa67c70babdaaad88d6eb81f4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755563"
---
# <a name="create-questionnaires"></a>Fragebögen erstellen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird der Prozess zum Erstellen eines Fragebogens beschrieben. Der erste Schritt ist das Entwerfen des Fragebogens. Wenn Sie einen Fragebogen entwerfen, schreiben Sie nicht nur Fragen und Antworten, Sie erstellen auch die Struktur, die es ermöglicht, Antworten zu erfassen und zu tabellieren. 

Mit einer sorgfältigen Gestaltung des Fragebogens sorgen Sie für eine bessere Qualität der gesammelten Daten. Durch sorgfältige Planung können Sie besser die geeigneten Optionen für einen Fragebogen zur richtigen Zeit auswählen. Die folgenden Punkte können Ihnen dabei helfen, einen effektiven Fragebogen zu planen:

-   Definieren Sie den Zweck des Fragebogens, um sicherzustellen, dass die Fragen diesen Zweck unterstützen.
-   Legen Sie die individuelle Person oder die Personengruppe fest, die den Fragebogen beantworten soll.
-   Arbeiten Sie Fragen aus, die im Fragebogen angezeigt werden und fügen Sie Antwort-Auswahlen ein, sofern zutreffend.
-   Stellen Sie sicher, dass der Fragebogen logisch verläuft, damit die Befragungsteilnehmer engagiert bleiben.
-   Ordnen Sie Fragen und Antworten in der Reihenfolge an, in der sie den Befragten angezeigt werden sollen.
-   Entscheiden Sie, sich wie die Ergebnisse ausgewertet werden sollen, sofern zutreffend.
-   Entscheiden Sie, ob Sie zusätzliche Features benötigen. Bestimmen Sie beispielsweise, ob und wie Ergebnisse kategorisiert werden sollen, ob ein Zeitlimit notwendig ist, oder ob alle Fragen verpflichtend sind.

Die Designphase umfasst vier Kategorien von Aufgaben, die in dieser Reihenfolge ausgeführt werden müssen:

1.  Voraussetzungen nach Bedarf einrichten.
2.  Antwortgruppen und Antworten einrichten, sofern zutreffend.
3.  Fragen und deren Zuordnung zu den Antwortgruppen einrichten.
4.  Den Fragebogen selbst einrichten und Fragen hinzufügen.

## <a name="prerequisites"></a>Erforderliche Komponenten
Bevor Sie Fragebögen, Antworten und Fragen einrichten können, müssen Sie einige Voraussetzungen erstellen. Für eine vollständige Funktionalität sind jedoch nicht alle Voraussetzungen notwendig.

### <a name="required"></a>Erforderlich

| Voraussetzung        | Beschreibung                |
|---------------------|----------------------------|
| Fragebogentypen | Fragebögen kategorisieren. |
| Fragetypen      | Fragen kategorisieren.      |

### <a name="optional"></a>Fakultativ

| Voraussetzung             | Beschreibung                                                    |
|--------------------------|----------------------------------------------------------------|
| Fragebogenparameter | Passen Sie grundlegende Steuerelemente und Standardeinstellungen für Fragebögen an. |

### <a name="questionnaire-types"></a>Fragebogentypen

Fragebogentypen sind erforderlich und müssen zugewiesen werden, wenn Sie einen Fragebogen erstellen. Fragebogentypen helfen Ihnen dabei, Fragebögen leichter zu verwalten und zu klassifizieren. Verwenden Sie Fragebogentypen, um Fragebögen zu klassifizieren und voneinander zu unterscheiden. Wenn Sie beispielsweise mehrere Fragebögen zur Auswahl haben, können Sie sie nach Typ filtern, um einen bestimmten Fragebogen leichter finden zu können. Beispiele für Fragebogentypen:

-   Personalverwaltung – Entwicklung
-   Kundenumfragen
-   Überprüfungsprozess

### <a name="question-types"></a>Fragetypen

Wenn Sie eine Frage erstellen, sind Fragebogentypen erforderlich und müssen zugewiesen werden. 

Verwenden Sie Fragentypen, die Fragen für die Berichterstellung kategorisieren. Fragetypen erleichtern es, nach Fragen zu suchen, da Sie Typen als Filter für die Seite **Fragen** verwenden können. Beispiele für Fragetypen:

-   Personalverwaltung
-   Geschäftsverwaltung
-   Kursbeurteilung

### <a name="questionnaire-parameters"></a>Fragebogenparameter

Fragebogenparametern sind optional. Je nach den Anforderungen Ihres Unternehmens kann es sein, dass Sie sie nicht verwenden. 

Fragebogenparameter definieren die Anonymität, die Nummernkreiscodes und die Referenztypen eines Fragebogens. Wenn eine Organisation einen Fragebogen verteilt, ist die Option, dass Teilnehmer anonym bleiben können, möglicherweise von Relevanz. 

Nummernkreiscodes werden verwendet, um Fragen und Antworten zu organisieren. Basierend auf diesen Nummernkreiscodes werden Werte automatisch diesen Elementen in zugewiesen. 

Alle Parameter sollten definiert worden sein, bevor Sie mit der Datenerstellung beginnen. Sie können die Fragebogenparametereinstellungen jederzeit ändern.

## <a name="questionnaire-components"></a>Fragebogen-Komponenten
Fragebögen enthalten drei wichtigste Elemente: Antwortgruppen, die für die Antworten Auswahlfragen, Fragen und Fragebogen selbst enthalten. Sie können die Fragen für einen Fragebogen optional in Ergebnisgruppen gruppieren. Mithilfe von Ergebnisgruppen können Sie Fragen kategorisieren und für weitere Analysen auf dem Fragebogen bereitstellen. 

[![QuestionnaireComponents.](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)

### <a name="answer-groups-and-answers"></a>Antwortgruppen und Antworten

Befragte haben je nach Inhalt der Frage zwei Möglichkeiten, diese zu beantworten:

-   Offene Fragen müssen nicht in einem bestimmten Format beantwortet werden. Befragte können in Form eines Texts, einer Zahl, eines Datums oder einer Uhrzeit antworten. Diese Fragen erfordern in der Regel, dass die Teilnehmer subjektive Informationen, wie etwa eine Meinung, eine Bewertung oder eine Schätzung eingeben.
-   Bei Fragen mit vordefinierten Antworten ist es erforderlich, dass der Befragte eine Antwort aus einer Liste möglicher richtiger Antworten auswählt.

Um eine Liste möglicher Antworten für Fragen mit vordefinierten Antworten verfügbar zu machen, können Sie Antworten auf der Seite **Antwortgruppen** erstellen 

Antwortgruppen und Antworten sind Komponenten der Informationen, aus denen Fragebögen erstellt werden. Nachdem Sie eine Antwortgruppe erstellt haben, können Sie sie im Feld **Antwortgruppe** auf der Seite **Fragen** einer Frage zuordnen. 

Eine Antwortgruppe kann für mehrere Fragen im gleichen Fragebogen oder in mehreren Fragebögen verwendet werden. 

> [!NOTE]
> Wenn Sie Antworttexte in den Antwortgruppen ändern, die bereits in ausgefüllten Fragebögen verwendet wurden, kann es schwierig werden, die Daten zu überprüfen und Fragebogenergebnisse sind möglicherweise nicht mehr gültig. Wenn Sie eine Antwortgruppe ändern müssen, sollten Sie erwägen, eine neue Antwortgruppe zu erstellen, anstatt eine vorhandene zu ändern. Antwortgruppen, die einer Frage oder Antwort zugeordnet sind oder bereits beantwortet wurden, können nicht gelöscht werden.

### <a name="questions"></a>Fragen

Fragebögen müssen Fragen beinhalten. Für Fragen können entweder offene Antworten oder vordefinierte Antworten zugelassen werden.

-   Die Antworten auf offene Fragen werden nicht gesteuert, sodass die Befragungsteilnehmer ihre die Antworten eingeben können.
-   Fragen mit vordefinierten Antworten setzen eine Liste mit vordefinierten Antwortoptionen voraus, und die Antworten können so strukturiert sein, dass die Befragten mehrere Antworten auswählen können. Fragen sollten so konzipiert werden, dass sie dem Befragten spezifische Informationen "entlocken" und müssen mit einer Antwortgruppe verknüpft sind, die die Antwortoptionen für jede Frage mit vordefinierten Antworten bereitstellt. 

    > [!NOTE]
    > Bevor Sie Fragen mit vordefinierten Antworten einrichten können, müssen Sie Antwortgruppen und Antworten erstellen.

Fragen können in einer Hierarchie aus bedingten Fragen angeordnet werden, sodass sekundäre Fragen von der Antwort abhängen, die von einem Befragungsteilnehmer für die vorherige Frage ausgewählt wurde. Sie können Fragen auch zuerst formulieren und später in einer Hierarchie anordnen.

## <a name="setting-up-questionnaires"></a>Erstellen von Fragebögen

> [!NOTE]
> Bevor Sie einen Fragebogen einrichten können, müssen Sie Fragen, Antworten und Voraussetzungen einrichten. 

Für jeden Fragebogen können folgende Informationen angegeben werden:

-   Die Gesamtzeit oder die Zeitgrenze zur Beantwortung obligatorischer Fragen.
-   Die Festlegung, ob alle Fragen obligatorisch sind.
-   Ob Punkte in einem Fragebogen berechnet werden.
-   Wie die Ergebnisse kategorisiert werden.
-   Ob der Fragebogen für eine eingeschränkten Gruppe an Befragten verfügbar ist.
-   Ob eine Formularvorlage als Hintergrund hinter jeder Fragebogenseite angezeigt werden soll.
-   Ob zusätzliche Hinweise benötigt werden, um den Befragten den Zweck des Fragebogens zu erläutern.
-   Ob die Fragen in einer bestimmten Reihenfolge angezeigt oder zufällig aus einem Pool ausgewählt werden sollen.
-   Ob Fragen nur gestellt werden, wenn bestimmte Antworten für vorherige Antworten gegeben wurden.

### <a name="set-up-a-questionnaire"></a>Einrichten eines Fragebogens

Die primäre Seite, die Sie verwenden, um einen Fragebogen einzurichten, ist die Seite **Fragebögen**. Um einen Fragebogen einzurichten, müssen Sie die folgenden Aufgaben der Reihe nach durchführen:

1.  Erstellen Sie einen Fragebogen.
2.  Führen Sie einen dieser Schritte aus, um Fragen des Fragebogens anzufügen:
    -   Sie können Fragen einem Fragebogen zuordnen, indem Sie Ergebnisgruppen verwenden. Erstellen Sie als Erstes die Ergebnisgruppen des Fragebogens und fügen Sie anschließend den Ergebnisgruppen Fragen hinzu.
    -   Wenn Sie keine Ergebnisgruppen verwenden, können Fragen dem Fragebogen direkt zugeordnet werden.

3.  Richten Sie bei Bedarf eine Hierarchie aus bedingten Fragen ein.
4.  Testen Sie den Fragebogen.

Klicken Sie auf der Seite **Fragebögen** auf **Überprüfen**, um festzustellen, dass der Fragebogen korrekt zusammengestellt ist. Es empfiehlt sich jedoch auch, den Fragebogen und den Test selbst durchzuführen, bevor Sie ihn verteilen.

### <a name="modify-a-questionnaire"></a>Modifizieren eines Fragebogens

Sie können auf der Seite **Fragebögen** die folgenden Aufgaben ausführen:

-   Modifizieren Sie Informationen im Fragebogen wie Ergebnisgruppen und Fragen.
-   Löschen und Hinzufügen von Fragen.
-   Vornehmen von Änderungen an den Ergebnisgruppen und der laufenden Nummer. 

> [!CAUTION]
> Seien Sie vorsichtig bei Änderungen an Fragebögen, die bereits beantwortet wurden. Änderungen können die Genauigkeit von Statistiken mindern und so eine unzulängliche Beurteilungsbasis schaffen. Es ist besser, eine neue Frage zu erstellen, als eine bereits beantwortete Frage zu ändern.

In einem Fragebogen können Sie die folgenden Typen von Fragen nicht löschen:

-   Fragen, die an einen Fragebogen angehängt sind
-   Fragen, die bereits beantwortet wurden und sich daher im Dialogfeld **Antworten** befinden.

### <a name="result-groups"></a>Ergebnisgruppen

Ergebnisgruppen sind optional, wenn Sie Fragen einem Fragebogen zuordnen. 

Eine Ergebnisgruppe wird verwendet, um Punkte zu berechnen und die Ergebnisse eines Fragebogens zu kategorisieren. Wenn Sie Ergebnisgruppen verwenden, können Sie die folgenden Aufgaben ausführen:

-   Fragebogenergebnisse auf Basis der Punktstatistiken auswerten.
-   Die Punktzahl eines Befragten für jede eingerichtete Ergebnisgruppe auswerten.
-   Sie können zur Vereinfachung der Analyse von Ergebnissen eine Statistik für die einzelnen Ergebnisgruppen generieren.
-   Einen Bericht drucken, der Ergebnisse für jede Ergebnisgruppe, sowie optionale Punkte/Texte auf der Grundlage der in jeder Ergebnisgruppe erzielten Punkte anzeigt.

> [!NOTE]
> Die folgenden Aufgaben müssen abgeschlossen werden, bevor Sie Ergebnisgruppen einrichten können:

-   Richten Sie Fragen mit vordefinierten Antworten ein. Für eine Frage mit vordefinierten Antworten muss der Eingabetyp auf der Seite **Fragen** entweder **Kontrollkästchen**, **Alternative Schaltfläche** oder **Eingabe-Listenfeld** sein .
-   Legen Sie Punkte für Antworten in Antwortgruppen fest, die den einzelnen Fragen zugewiesen sind.
-   Richten Sie einen Fragebogen ein.

Um Fragen zu einem Fragebogen mit Ergebnisgruppen hinzuzufügen, richten Sie zuerst die Ergebnisgruppen für den Fragebogen ein, und fügen Sie den Ergebnisgruppen dann Fragen hinzu. Wenn Sie keine Ergebnisgruppen verwenden, können Fragen dem Fragebogen direkt zugeordnet werden. 

Sie können mehrere Ergebnisgruppen einrichten, um die Punkte zu überprüfen, die ein Teilnehmer in jeder Kategorie erworben hat. Nachdem ein Fragebogen ausgefüllt wurde, können Sie die Punkte anzeigen, die für jede Ergebnisgruppe erreicht wurden. 

> [!TIP]
> Um einen Fragebogen mithilfe der Punkte, aber nicht separater Kategorien, zu bewerten, können Sie alle Fragen einer einzelnen Ergebnisgruppe hinzufügen. 

Für jede Ergebnisgruppe können Sie einen oder mehrere punktbasierte Nachrichten einrichten, die einem Teilnehmer nach Beantwortung des Fragebogens angezeigt werden. Der angezeigte Text kann je nach erreichter Punktzahl des Befragten in einer Ergebnisgruppe unterschiedlich sein. Um punktbasierte Nachrichten zu verwenden, müssen Sie Punktintervalle sowie eine Beschreibung für jedes Intervall definieren. Wenn die Punktzahl eines Befragten in einem bestimmten Intervall liegt, wird der Text für dieses Intervall in den Ergebnisbericht aufgenommen. 

Da sich eine Ergebnisgruppe auf Punkte bezieht, die zu einer bestimmten Gruppe von Fragen auf einem Fragebogen gehören, können Sie für einen Fragebogen nur eine spezifische Ergebnisgruppe verwenden.

#### <a name="example-pointstexts-for-result-group-3"></a>Beispiel: Punkte/Text für die Ergebnisgruppe "3"

Sie verwenden einen Fragebogen für einen Führungstest, der über 15 Fragen in drei Kategorien verfügt. Sie erstellen drei Ergebnisgruppen und fügen fünf Fragen jeder Ergebnisgruppe hinzu. Punkte werden dann in den drei Gruppen summiert. Die drei Ergebnisgruppen sind wie folgt:

-   Kreative Fähigkeiten
-   Führungsqualitäten
-   Technische Fähigkeiten

Um punktbasierte Nachrichten zu verwenden, können Sie Textintervalle für jede Ergebnisgruppe einrichten. Jeder Frage werden zwei Punkte zugewiesen. Daher ist die maximale Gesamtpunktzahl in einer Ergebnisgruppe 10. 

Die folgende Tabelle zeigt die punktbasierten Nachrichten, die Sie für die "Führungsmöglichkeits-Ergebnisgruppe" definieren.

| Punktintervall | Text                                       |
|----------------|--------------------------------------------|
| 1 bis 3         | Sie haben durchschnittliche Führungsqualitäten.     |
| 4 bis 7         | Sie haben gute Führungsqualitäten.        |
| 8 bis 10        | Sie haben hervorragende Führungsqualitäten. |

Sie können Punktintervalle und Texte für die einzelnen Ergebnisgruppen in einem Fragebogen einrichten. Texte, die der Punktzahl jedes Befragten entsprechen, werden für jede Ergebnisgruppe angezeigt. 

> [!NOTE]
> Sie können Intervalle und Texte ändern. Wenn ein Fragebogen jedoch abgeschlossen wurde, können Änderungen zu Diskrepanzen zwischen alten und neuen Ergebnisberichten führen.

### <a name="conditional-question-hierarchies"></a>Bedingte Fragenhierarchien

Bedingte Fragenhierarchien sind optional, wenn Sie einen Fragebogen einrichten. 

> [!NOTE]
> Bevor Sie eine Hierarchie aus bedingten Fragen einrichten können, müssen dem Fragebogen bereits Fragen zugeordnet sein, mit denen Antwortgruppen verknüpft sind. 

Um mithilfe bedingter Fragen eine Fragenhierarchie in einem Fragebogen zu erstellen, können Sie die Reihenfolge, in der die Fragen präsentiert werden, von den Antworten abhängig machen, die von einem Befragten für die verschiedenen Fragen ausgewählt werden. Somit können Sie den Fragebogen an den Befragten anpassen.

#### <a name="examples"></a>Beispiele

Eine juristische Person bietet seinen Kunden sowohl Artikel als auch Dienstleistungen an. Typischer Weise kaufen einige Kunden nur Artikel oder nur Dienstleistungen und manche beides. Wenn die juristische Person eine Umfrage zur Kundenzufriedenheit verteilt, kann mithilfe einer bedingten Struktur des Fragebogens verhindert werden, sodass Kunden, die nur Dienstleistungen kaufen, Fragen zu Artikeln beantworten müssen. 

Alternativ können Sie einen Fragebogen z. B. so einrichten, dass Frage 2 die nächste Frage in der Folge ist, wenn ein Befragter die Antwort A für Frage 1 auswählt. Wenn der Befragte Antwort B für Frage 1 auswählt, dann könnte Frage 5 als nächstes folgen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]