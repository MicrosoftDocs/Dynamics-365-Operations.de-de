---
title: Meilensteinvorlagen
description: In diesem Thema wird erklärt, wie Sie die Meilenstein-Abrechnungsfunktionalität in Abonnement-Abrechnung festlegen.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: ecc4ddbb4d22eefac36f8cf8205d3b6084bd7d9d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686490"
---
# <a name="milestone-billing"></a>Meilenstein Abrechnung

[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie Sie Vorlagen für die Meilenstein-Abrechnungsfunktion in Abonnement-Abrechnung definieren. Für jede Zeile in der Meilenstein-Vorlage können Sie den Zuordnungsprozentsatz oder den Betrag festlegen. Sie können die Meilenstein-Vorlage dann Abrechnungsplanpositionen zuordnen, die die Meilenstein-Abrechnungsfunktionalität verwenden.

## <a name="add-a-template"></a>Eine Vorlage hinzufügen

Gehen Sie folgendermaßen vor, um eine Meilenstein-Vorlage hinzuzufügen.

1. Gehen Sie zu **Abonnement Abrechnung \> Wiederkehrende Vertragsabrechnung \> Einrichtung \> Meilenstein Vorlagen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie in das Feld **Meilenstein Vorlage** einen eindeutigen Bezeichner für die neue Vorlage ein.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
5. Wählen Sie im Feld **Zuordnungsmethode** eine Zuordnungsmethode aus.
6. Optional: Geben Sie im Feld **Gesamtbetrag** den Gesamtbetrag für die Vorlage an.
7. Um eine Zeile hinzuzufügen, wählen Sie **Hinzufügen**. Wählen Sie dann im Feld **Positionsnummer** die Positionsnummer für die neue Zeile.
8. Führen Sie einen dieser Schritte aus, je nach dem Wert, den Sie im Feld **Zuweisungsmethode** ausgewählt haben:

    - Wenn Sie **Prozentsatz** als Zuordnungsmethode gewählt haben, geben Sie im Feld **Prozentsatz** den Zuordnungsprozentsatz für jede Zeile an. Wenn Sie Prozentsätze angeben, muss die Summe der Prozentsätze, die im Feld **Gesamtprozentsatz** angezeigt wird, gleich **100** sein.
    - Wenn Sie **Variabler Betrag** als Zuweisungsmethode gewählt haben, geben Sie im Feld **Betrag** den Betrag für jede Zeile an.
    - Wenn Sie **Gleicher Betrag** als Zuweisungsmethode gewählt haben, müssen Sie keinen Betrag angeben. Jede Zeile wird mit dem richtigen Prozentsatz und Betrag aktualisiert, basierend auf der Anzahl der Elemente, die der Vorlage hinzugefügt werden.

9. Wählen Sie **Speichern** aus.

## <a name="delete-a-template"></a>Eine Vorlage löschen

Um eine Meilenstein-Vorlage zu löschen, gehen Sie wie folgt vor.

1. Markieren Sie eine oder mehrere zu löschende Zeilen und wählen Sie dann **Löschen**.
2. Wenn Sie aufgefordert werden, die Aktion zu bestätigen, wählen Sie **Ja**.

## <a name="milestone-template-fields"></a>Felder für Meilenstein-Vorlagen

Die Seite **Meilenstein Vorlage** enthält die folgenden Felder.

| Feld | Description |
|-------|-------------| 
| Meilensteinvorlage | Der eindeutige Bezeichner der Meilenstein-Vorlage. |
| Description | Die Beschreibung der Meilenstein-Vorlage. |
| Zuordnungsmethode | <p>Wählen Sie die Zuordnungsmethode:</p><ul><li>**Prozentsatz der Fertigstellung** - Für jede Zeile wird ein kumulativer Fertigstellungswert verwendet.</li><li>**Prozentsatz** - Es kann ein prozentualer Betrag für die Zuordnung angegeben werden. Die Summe aller Prozentsätze muss gleich 100 sein.</li><li>**Variabler Betrag** - Es kann ein Betrag für die Umlage angegeben werden. Der Zuweisungsbetrag wird auf der Ebene der Transaktion angegeben.</li><li>**Gleicher Betrag** - Die Zuweisungsprozentsätze werden automatisch berechnet und gleichmäßig auf die Elemente in der Vorlage aufgeteilt.</li></ul> |
| Gesamtzahl | Geben Sie den Meilensteinbetrag für die Vorlage an. |
| **Positionen** | |
| Artikelnummer | Wählen Sie die Elementnummer für die Meilenstein-Vorlage. |
| Produktname | Der Name des Artikels. |
| Prozentsatz | <p>Geben Sie den Zuweisungsprozentsatz für die Zeile ein:</p><ul><li>Wenn das Feld **Zuordnungsmethode** auf **Prozentsatz** festgelegt ist, geben Sie den Prozentsatz für die Zeile an.</li><li>Wenn das Feld **Zuweisungsmethode** auf **Gleicher Betrag** festgelegt ist, wird der Prozentsatz automatisch in gleiche Prozentsätze aufgeteilt, basierend auf der Anzahl der Elemente in der Vorlage.</li></ul><p>Die Summe aller Prozentsätze muss gleich 100 sein.</p><p>Wenn in der Kopfzeile ein Wert **Gesamtbetrag** angegeben ist und Sie den Wert **Prozentsatz** für die Zeile ändern, wird der Wert **Betrag** aktualisiert. Umgekehrt wird, wenn Sie den Wert **Betrag** ändern, der Wert **Prozentsatz** aktualisiert.</p> |
| Betrag | <p>Der Zuweisungsbetrag für die Zeile:</p><ul><li>Wenn das Feld **Zuordnungsmethode** auf **Variabler Betrag** festgelegt ist, geben Sie den Betrag für die Zeile an.</li><li>Wenn das Feld **Zuweisungsmethode** auf **Gleicher Betrag** festgelegt ist, wird der Betrag automatisch in gleiche Beträge aufgeteilt, basierend auf der Anzahl der Elemente in der Vorlage und dem Wert **Gesamtbetrag**, der in der Kopfzeile angegeben ist.</li></ul><p>Die Summe aller Beträge muss dem Wert **Gesamtbetrag** entsprechen, der in der Kopfzeile angegeben ist.</p><p>Wenn in der Kopfzeile ein **Gesamtbetrag** angegeben ist und Sie den Wert **Betrag** für die Zeile ändern, wird der Wert **Prozentsatz** aktualisiert. Umgekehrt, wenn Sie den **Prozentsatz** Wert ändern, wird der **Betrag** Wert aktualisiert.</p> |
| **Summen** | |
| Gesamter Prozentsatz | Die Summe der Prozentsätze. Die Summe aller Prozentsätze muss gleich 100 sein. |
| Gesamtzahl | Die Summe der **Betrag** Werte für alle Zeilen. Diese Summe muss dem Wert **Gesamtbetrag** entsprechen, der in der Kopfzeile angegeben ist. |
| Verbleibender Betrag | Der Restbetrag. Der Wert wird berechnet als der **Gesamtbetrag**-Wert aus der Kopfzeile minus der Summe der **Betrag**-Werte für alle Zeilen.|

## <a name="milestone-allocation"></a>Meilensteinzuteilung

Bevor Sie die Meilenstein-Funktionalität nutzen können, sollten Sie diese Aufgaben erledigen.

1. Fügen Sie eine oder mehrere Meilenstein-Vorlagen hinzu.
2. Erstellen Sie eine Abrechnungsplangruppe. Geben Sie **Meilenstein** als Elementtyp an und wählen Sie eine Vorlage.
3. Wählen Sie auf der Seite **Einrichtung eines Elements** (**Abonnementabrechnung \> Wiederkehrende Vertragsabrechnung \> Einrichtung \> Elemente**) eine Elementbeziehung und eine Meilensteinvorlage für die Elementeinrichtung aus.

Nachdem Sie die Meilensteinvorlagen, Abrechnungsplangruppen und Elemente erstellt haben, können Sie einen Abrechnungsplan erstellen, der die Meilensteinfunktionalität verwendet.

Um einen Abrechnungsplan festzulegen, der Meilensteine verwendet, gehen Sie folgendermaßen vor.

1. Wählen Sie aus der Liste **Alle/Aktive Abrechnungspläne** auf der Seite **Abrechnungspläne** die Option **Neu**.
2. Erstellen Sie auf der Seite **Alle Abrechnungspläne** einen neuen Abrechnungsplan und geben Sie ein Kundenkonto und ein Startdatum an.
3. Im Bereich **Fakturierungseinteilungen** wählen Sie **Zeile hinzufügen**. Fügen Sie dann eine Elementnummer hinzu und legen Sie im Feld **Elementtyp** den Wert **Meilenstein** fest.

    Wenn für das Element eine Standard-Meilensteinvorlage festgelegt ist, werden die Meilenstein-Ereignisse automatisch zu den Rechnungseinteilungen hinzugefügt. Enddaten sind für Meilenstein-Zeilen leer.

    Wenn für das Element keine Meilenstein-Vorlage festgelegt ist, wählen Sie **Meilenstein-Zuordnung**. Wählen Sie dann auf der Seite **Meilensteinzuordnung** eine Meilensteinvorlage aus und nehmen Sie alle erforderlichen Aktualisierungen vor. Wählen Sie dann **Schließen**, um zum Rechnungsplan zurückzukehren und das Erstellen des Rechnungsplans abzuschließen.

4. Um Rechnungen für den Abrechnungsplan zu erstellen, müssen Sie das Enddatum für jedes Meilenstein-Ereignis aktualisieren. Für einen einzelnen Fakturierungsplan können Sie das Enddatum für das Ereignis Meilenstein in den Fakturierungseinteilungen aktualisieren. Um mehrere Fakturierungszeitpläne zu aktualisieren, wählen Sie **Abschlussdatum Prozess aktualisieren**.
5. Nachdem das Enddatum aktualisiert wurde, können Sie die Rechnung erstellen. Für einen einzelnen Fakturierungsplan wählen Sie **Rechnung generieren** auf der Seite **Alle Fakturierungspläne**. Um Rechnungen für mehrere Abrechnungspläne zu erstellen, wählen Sie **Rechnung erstellen** oder **Rechnung erstellen Batch-Verarbeitung** unter **Periodische Aufgaben**.

## <a name="edit-milestone-allocation-on-a-billing-schedule-line"></a>Bearbeiten Sie die Zuordnung von Meilensteinen in einer Rechnungseinteilung

So bearbeiten Sie die Meilensteinzuordnung in einer Rechnungseinteilung.

1. Wählen Sie auf der Seite **Abrechnungszeitpläne** > **Alle oder aktive Abrechnungszeitpläne** im Feld **Zeitplannummer** die Zeitplannummer des Abrechnungszeitplans.
2. Geben Sie im Bereich **Fakturierungseinteilungen** ein Element ein, geben Sie als Element **Meilenstein** an und wählen Sie **Meilenstein-Zuordnung**.
3. Wählen Sie im Feld **Meilenstein-Vorlage** eine Meilenstein-Vorlage aus.
4. Wählen Sie **Verarbeiten** aus. Die Meilenstein-Vorlagenzeilen werden automatisch zu den Rechnungseinteilungen hinzugefügt.

## <a name="milestone-allocation-fields"></a>Felder für die Zuweisung von Meilensteinen

Die Seite **Meilensteinzuweisung** enthält die folgenden Felder.

| Feld | Description |
|-------|-------------|
| Übergeordneter Artikel | Die Elementnummer des übergeordneten Elements. |
| Erweiterter Preis | <p>Der erweiterte Preis des Elements. Der Wert entspricht dem Wert **Nettobetrag** der Rechnungseinteilung.</p></p>Für ein übergeordnetes Element eines Meilensteins ist der Standardwert der **Gesamtbetrag**, der für die Meilensteinvorlage angegeben ist. Wenn der Gesamtbetrag 0 (Null) ist, ist der Standardwert der **Nettobetrag** der Rechnungseinteilung.</p> |
| Meilensteinvorlage | Die Meilenstein-Vorlagen-ID der Zeile. |
| Vorlagenbeschreibung | Die Beschreibung der Meilenstein-Vorlage. |
| Zuordnungsmethode | Die Zuweisungsmethode, die für die Meilensteinvorlage verwendet wird. |
| **Linien** | Die Standardwerte für alle Zeilen basieren auf der ausgewählten Meilenstein-Vorlage. Sie können sie nach Bedarf ändern. |
| Artikelnummer | Die Elementnummer für die Meilenstein-Zuordnungsvorlage. |
| Produktname | Der Produktname. |
| Prozentsatz | <p>Der Zuweisungsprozentsatz für die Zeile. Die Summe aller Prozentsätze muss gleich 100 sein.</p><p>Wenn Sie den Wert **Prozentsatz** für die Zeile ändern, wird der Wert **Nettobetrag** aktualisiert. Umgekehrt, wenn Sie den Wert **Nettobetrag** ändern, wird der **Prozentsatz** aktualisiert.</p> |
| Nettobetrag | <p>Der Zuweisungsbetrag für die Zeile. Die Summe der Nettobeträge für alle Zeilen muss dem **Erweiterten Preis** entsprechen, der in der Kopfzeile angegeben ist.</p><p>Wenn Sie den Wert **Nettobetrag** für die Zeile ändern, wird der Wert **Prozentsatz** aktualisiert. Umgekehrt wird, wenn Sie den Wert **Prozentsatz** ändern, der Wert **Nettobetrag** aktualisiert.</p> |
| **Summen** | |
| Gesamter Prozentsatz | Die Summe der **Prozentsatz**-Werte für alle Zeilen. Diese Summe muss gleich 100 sein. |
| Gesamtzahl | Die Summe der **Nettobetrag**-Werte für alle Zeilen. Diese Summe muss dem Wert **Erweiterter Preis** entsprechen, der in der Kopfzeile angegeben ist. |
| Verbleibender Betrag | Der Restbetrag. Der Wert wird berechnet als der **Erweiterter Preis** Wert aus der Kopfzeile minus der Summe der **Nettobetrag** Werte für alle Zeilen. Der Endbetrag muss 0 (Null) sein. |
