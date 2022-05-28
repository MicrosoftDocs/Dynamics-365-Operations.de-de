---
title: Kategorieanfragen von Kreditoren
description: Dieses Thema beschreibt, wie Kreditor Beschaffungskategorien für sein Konto anfordern kann. Es beschreibt auch den Genehmigungsprozess, der von Beschaffungsbeauftragten durchgeführt wird.
author: GalynaFedorova
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9874151a5d82cc3441741489065877b78bab7bf5
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671196"
---
# <a name="category-requests-from-vendors"></a>Kategorieanfragen von Kreditoren

[!include [banner](../includes/banner.md)]

Mit dem Kategorieanforderungsprozess können Kreditor beantragen, dass neue Beschaffungskategorien mit ihrem Konto verknüpft werden. Diese Beschaffungskategorien können dann von den entsprechenden Beschaffungs- und Beschaffungsprozessen verwendet werden. (Weitere Informationen finden Sie unter [Beschaffungskataloge im Überblick](procurement-catalogs.md).)

Kategorieanfragen werden von Kreditoren im Arbeitsbereich **Kreditoreninformationen** initiiert. Sie werden dann an Ihre Behörde zur Überprüfung und Genehmigung gesendet. Genehmigte Kategorien werden der Liste der Beschaffungskategorien für das Konto des Lieferanten hinzugefügt.

## <a name="turn-the-category-requests-from-vendors-feature-on-or-off"></a>Kategorieanforderungen von Kreditoren ein- oder ausschalten

Ab Supply Chain Management Version 10.0.25 ist diese Funktion standardmäßig aktiviert. Administratoren können diese Funktion ein- oder ausschalten, indem sie nach der Funktion *Kreditoren erlauben, sich über Kreditorenzusammenarbeit für Beschaffungskategorien zu bewerben* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

Wenn diese Funktion eingeschaltet ist, können Sie immer noch manuell Beschaffungskategorien zu Kreditorenkonten hinzufügen. Informationen finden Sie unter [Kreditoren für bestimmte Beschaffungskategorien genehmigen](tasks/approve-vendors-specific-procurement-categories.md).

## <a name="vendor-collaboration-requirements"></a>Anforderungen an die Zusammenarbeit mit dem Kreditor

Bevor ein Verkäufer mit Kategorieanforderungen interagieren kann, muss er für die Zusammenarbeit mit Verkäufern festgelegt werden.

Der Kreditor muss mindestens einen Benutzer für die Zusammenarbeit mit Lieferanten haben. Nur Kreditorenbenutzer mit der Sicherheitsrolle *Kreditorenadministrator (extern)* kann Kategorieanforderungen erstellen und senden.

Weitere Informationen finden Sie unter [Kreditorenzusammenarbeit einrichten und verwalten](set-up-maintain-vendor-collaboration.md).

## <a name="set-up-the-vendor-category-request-workflow"></a>Festlegen des Workflows für Kreditor-Kategorie-Anforderungen

Der *Lieferantenkategorie-Anfrage* Workflow muss in den Beschaffungs- und Sourcing-Workflows festgelegt werden. Kreditor sendet neue Kategorieanforderungen, die Sie überprüfen und genehmigen können. Angeforderte Beschaffungskategorien werden zu einem Kreditor-Konto hinzugefügt, nachdem eine Kategorie-Anforderung genehmigt wurde.

Das folgende Beispiel zeigt, wie Sie einen einfachen *Kreditoren-Kategorie-Antrag*-Workflow festlegen, der einen einzigen Genehmiger hat. Sie müssen Ihre internen Prozesse überprüfen, um den geeigneten Workflow für Ihre Agentur einzurichten.

1. Gehen Sie zu **Beschaffung und Beschaffung \> Einrichten \> Beschaffungs- und Beschaffungsworkflows**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie im Dialogfeld die Option **Workflow für Lieferantenkategorie anfordern**, um den Workflow-Editor zu öffnen.
1. Melden Sie sich am Workflow-Editor an.
1. Wählen Sie im Aktivitätsbereich **Eigenschaften**.
1. Geben Sie auf der Seite **Eigenschaften** für den Workflow, im Feld **Einreichungsanweisungen**, Anweisungstext ein. Die Anweisungen werden für Kreditor sichtbar, wenn sie eine Kategorie-Anfrage senden.
1. Schließen Sie die Seite **Eigenschaften**.
1. Ziehen Sie das Workflow-Element **Neue Kategorieanforderung genehmigen** auf den Canvas.
1. Ziehen Sie eine Verknüpfung vom Workflow-Element **Start** zum Workflow-Element **Neue Kategorieanforderung genehmigen**.
1. Ziehen Sie einen Link vom Workflow-Element **Neue Kategorieanforderung genehmigen** zum Workflow-Element **Ende**.
1. Tippen Sie doppelt auf (oder doppelklicken Sie auf) das Workflow-Element **Neue Kategorieanforderung genehmigen**.
1. Wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) das Workflow-Element **Schritt 1** und wählen Sie dann **Eigenschaften**.
1. Auf der Seite **Eigenschaften** für das Workflow-Element geben Sie im Feld **Bearbeitungsgegenstand** einen Betrefftext ein. Dieser Text wird als Wert des Feldes **Betreff** auf der Seite **Mir zugewiesene Aufträge** angezeigt.
1. Geben Sie im Feld **Arbeitselement-Anweisungen** einen Anweisungstext ein. Die Anweisungen werden für Genehmiger sichtbar, wenn sie **Workflow** im Aktivitätsbereich einer Kategorie-Anfrage wählen.
1. Wählen Sie im linken Fensterbereich **Zuordnung**.
1. Legen Sie auf der Registerkarte **Zuweisungstyp** **Benutzer zu diesem Workflow-Element zuweisen** auf *Benutzer* fest.
1. Wählen Sie auf der Registerkarte **Benutzer** in der Liste **Verfügbare Benutzer** einen Genehmiger aus. Wählen Sie zum Beispiel einen Benutzer in der Beschaffungsabteilung.
1. Wählen Sie die rechte Pfeilschaltfläche (**\>**), um den Genehmiger in die Liste **Ausgewählte Benutzer** zu verschieben.
1. Schließen Sie die Seite **Eigenschaften**.
1. Wählen Sie **Speichern und schließen**.
1. Geben Sie im Feld **Versionshinweise** Notizen zum Workflow ein.
1. Wählen Sie **OK**, um den Workflow zu speichern.
1. Wenn Sie bereit sind, mit dem Testen des Workflows zu beginnen, wählen Sie **Aktivieren Sie die neue Version**. Andernfalls wählen Sie **Nicht die neue Version aktivieren**.
1. Wählen Sie **OK**, um das Einrichten des Workflows abzuschließen.

> [!TIP]
> Wenn Ihre Agentur keine Genehmigung von Kategorieanfragen verlangt, sollten Sie den Workflow für eine automatische Genehmigung konfigurieren.

Weitere Informationen darüber, wie Sie Workflows festlegen, finden Sie unter [Workflow-Systemübersicht](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

## <a name="create-and-submit-a-category-request"></a>Erstellen und Senden einer Kategorieanforderung

Dieser Abschnitt beschreibt, wie Kreditor den Arbeitsbereich **Lieferanteninformationen** verwenden kann, um Kategorieanfragen zu erstellen, zu bearbeiten, anzuzeigen und zu senden.

### <a name="start-a-new-request"></a>Starten Sie eine neue Anfrage

Um eine neue Kategorieanforderung zu starten, führen Sie diese Schritte aus.

1. Wählen Sie im Arbeitsbereich **Lieferanteninformationen** die Kachel **Kategorie Anfragen**.
1. Wählen Sie auf der Seite **Kategorieanforderungen** im Aktivitätsbereich **Neue Kategorieanforderung**.
1. Suchen Sie im Dialogfeld **Anforderung einer neuen Kategorie** die Kategorie, für die Sie sich bewerben möchten, indem Sie im Baum navigieren und/oder den Filter am oberen Rand der Liste verwenden. Aktivieren Sie das Kontrollkästchen für jede relevante Kategorie.

    Beachten Sie die folgenden Punkte:

    - Kategorien, die derzeit in Ihrem Kreditor-Konto aktiv sind, werden als ausgewählt angezeigt und können nicht entfernt werden.
    - Sie können mehrere Beschaffungskategorien in einer einzigen Kategorieanforderung anfordern.

1. Wählen Sie **OK**, um den Antragsentwurf zu erstellen.

    Die neue Entwurfsanforderung erscheint jetzt auf der Seite **Kategorieanforderungen**.

1. Öffnen Sie den neuen Anforderungsentwurf, um ihn zu überprüfen und bei Bedarf zu bearbeiten.

    - Um die Liste der Kategorien zu sehen, die aktuell in der Anfrage enthalten sind, wählen Sie das **Angeforderte Kategorien** Inforegister.
    - Um die aktiven Kategorien zu sehen, öffnen Sie die **Aktive Kategorien** FactBox auf der rechten Seite der Seite.
    - Um eine Kategorie zur Anforderung hinzuzufügen, wählen Sie **Hinzufügen** in der Symbolleiste auf dem Inforegister **Angeforderte Kategorien**.
    - Um eine Kategorie aus der Anforderung zu entfernen, wählen Sie die Kategorie auf der Inforegister-Registerkarte **Angeforderte Kategorien** aus und wählen dann **Entfernen** in der Symbolleiste.
    - Um ein Dokument an die Anfrage anzuhängen, wählen Sie **Anhänge** im Aktivitätsbereich. Die angehängten Dokumente stehen den Genehmigern zur Verfügung, wenn sie die Kategorieanforderung überprüfen.
    - Um ein angehängtes Dokument aus der Anforderung zu entfernen, wählen Sie **Anhänge** im Aktivitätsbereich. Wählen Sie das Dokument aus, das Sie entfernen möchten, und wählen Sie dann **Löschen** im Aktivitätsbereich.

1. Wenn Sie bereit sind, den Antrag zu senden, wählen Sie **Senden** im Aktivitätsbereich. Andernfalls schließen Sie einfach die Seite und überspringen Sie die restlichen Schritte dieses Vorgangs. Sie können dann später zu dem Auftrag zurückkehren.
1. Lesen Sie alle angezeigten Anweisungen zum Senden und wählen Sie dann **Senden**.
1. Geben Sie in das Feld **Kommentar** die gewünschten Zusatzinformationen ein. Wählen Sie dann **Senden**, um die Anfrage abzuschließen.

### <a name="edit-a-draft-or-recalled-request"></a>Bearbeiten eines Entwurfs oder einer zurückgerufenen Anfrage

Um einen Entwurf oder eine abgerufene Kategorieanforderung zu bearbeiten, gehen Sie wie folgt vor.

1. Wählen Sie im Arbeitsbereich **Lieferanteninformationen** die Kachel **Kategorie Anfragen**.
1. Wählen Sie den Entwurf oder die abgerufene Anfrage, um sie zu öffnen.
1. Bearbeiten Sie die Anfrage wie gewünscht und schließen Sie sie dann entweder oder senden Sie sie wie im vorherigen Verfahren beschrieben.

### <a name="submit-a-draft-or-recalled-request"></a>Entwurf oder Rückrufauftrag senden

Um einen Entwurf oder eine zurückgerufene Kategorieanforderung zu senden, führen Sie diese Schritte aus.

1. Wählen Sie im Arbeitsbereich **Lieferanteninformationen** die Kachel **Kategorie Anfragen**.
1. Wählen Sie den Entwurf oder die abgerufene Anforderung, die Sie senden wollen.
1. Wählen Sie im Aktivitätsbereich **Senden**.
1. Lesen Sie alle angezeigten Anweisungen zum Senden und wählen Sie dann **Senden**.
1. Geben Sie in das Feld **Kommentar** die gewünschten Zusatzinformationen ein. Wählen Sie dann **Senden**, um die Anfrage abzuschließen.

    Der Status der Kategorie-Anfrage wird auf einen der folgenden Werte geändert:

    - _Ausstehende Überprüfung_ – Die Anforderung befindet sich im Workflow.
    - _Ausstehende Genehmigung_ – Eine Genehmigung ist erforderlich.

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a>Rückruf einer gesendeten Anfrage, die noch nicht genehmigt wurde

Um eine Kategorie-Anfrage zurückzurufen, die gesendet, aber noch nicht genehmigt wurde, führen Sie diese Schritte aus.

1. Wählen Sie im Arbeitsbereich **Lieferanteninformationen** die Kachel **Kategorie Anfragen**.
1. Wählen Sie die ausstehende Anforderung, die Sie zurückrufen möchten.
1. Wählen Sie im Aktivitätsbereich **Abrufen**.
1. Geben Sie in das Feld **Kommentar eingeben** alle erforderlichen Zusatzinformationen ein. Wählen Sie dann **Senden**, um die Anfrage abzuschließen.

    Der Status der Kategorie-Anfrage wird auf _Storniert_ geändert. Die Anforderung bleibt in diesem Status, bis Sie sie löschen oder erneut übermitteln.

### <a name="delete-a-draft-or-recalled-request"></a>Löschen eines Entwurfs oder einer zurückgerufenen Anforderung

Um einen Entwurf oder eine zurückgerufene Kategorieanforderung zu löschen, führen Sie diese Schritte aus.

1. Wählen Sie im Arbeitsbereich **Lieferanteninformationen** die Kachel **Kategorie Anfragen**.
1. Wählen Sie den Entwurf oder die abgerufene Anforderung, die Sie löschen möchten.
1. Wählen Sie im Aktivitätsbereich **Löschen**.
1. Wählen Sie **Ja** aus, um das Löschen zu bestätigen.

### <a name="view-completed-requests"></a>Abgeschlossene Anfragen anzeigen

Um abgeschlossene Anfragen anzuzeigen, öffnen Sie den Arbeitsbereich **Lieferanteninformationen** und wählen die Kachel **Kategorieanfragen**. Kategorieanfragen, die abgeschlossen wurden, haben einen der folgenden Status:

- _Genehmigt_ – Die Anfrage wurde genehmigt. Um die neu hinzugefügten Kategorien anzuzeigen, gehen Sie zurück in den Arbeitsbereich **Lieferanteninformationen**, öffnen die Dropdown-Liste **Weitere Details** im linken Fensterbereich und wählen dann **Kategorien**.
- _Abgelehnt_ – Die Anfrage wurde abgelehnt. Sie können bei Bedarf eine neue Kategorie-Anfrage erstellen.

## <a name="review-category-requests"></a>Überprüfen der Kategorieanforderungen

Dieser Abschnitt erklärt, wie Sie Kategorie-Anfragen, die Kreditor gesendet hat, genehmigen, ablehnen und delegieren können und wie Sie abgeschlossene Anfragen ansehen können. Diese Workflow-Aktionen beziehen sich auf den gesamten Kategorieauftrag.

### <a name="view-category-requests"></a>Anzeigen von Kategorieaufträgen

Um Anfragen der Kategorie anzuzeigen, gehen Sie wie folgt vor.

1. Gehen Sie zu **Beschaffung und Bezugsquellenfindung \> Lieferanten \> Anfragen zur Zusammenarbeit mit Lieferanten \> Kategorie-Anfragen**.

    Die Seite **Kategorieanforderungen** erscheint. Die Standardseitenansicht zeigt Kategorieanfragen, die den Status *Ausstehende Aktion* haben.

1. Um alle Aufträge anzuzeigen, wählen Sie *Alle* im Feld **Aufträge anzeigen**.
1. Öffnen Sie eine Anfrage, um sie zu überprüfen und bei Bedarf zu bearbeiten.

    - Um die Liste der Kategorien zu sehen, die aktuell in der Anfrage enthalten sind, wählen Sie das **Angeforderte Kategorien** Inforegister.
    - Um die aktiven Kategorien zu sehen, öffnen Sie die **Aktive Kategorien** FactBox auf der rechten Seite der Seite.
    - Wenn Dokumente gesendet wurden, zeigt die Schaltfläche **Anhänge** (Büroklammer) im Aktivitätsbereich eine Anzahl der angehängten Dokumente an. Um angehängte Dokumente anzuzeigen, wählen Sie die Schaltfläche **Anhänge**. Wählen Sie dann das zu betrachtende Dokument und wählen Sie **Öffnen**, um es zu betrachten.
    - Um ein Dokument an die Anfrage anzuhängen, wählen Sie **Anhänge** im Aktivitätsbereich. Die angehängten Dokumente stehen den Genehmigern zur Verfügung, wenn sie die Kategorieanforderung überprüfen.
    - Um ein angehängtes Dokument aus der Anforderung zu entfernen, wählen Sie **Anhänge** im Aktivitätsbereich. Wählen Sie das Dokument aus, das Sie entfernen möchten, und wählen Sie dann **Löschen** im Aktivitätsbereich.
    - Um die Workflow-Historie anzuzeigen, wählen Sie **Workflow** im Aktivitätsbereich. Wählen Sie in den Workflow-Optionen **Mehr** und dann **Workflowverlauf**. Die Seite **Workflow-Historie** erscheint.

### <a name="approve-a-pending-category-request"></a>Genehmigen Sie eine ausstehende Kategorie-Anfrage

Um eine ausstehende Kategorie-Anforderung zu genehmigen, führen Sie diese Schritte aus.

1. Gehen Sie zu **Beschaffung und Bezugsquellenfindung \> Lieferanten \> Anfragen zur Zusammenarbeit mit Lieferanten \> Kategorie-Anfragen**.
1. Wählen Sie die ausstehende Anfrage, die Sie genehmigen möchten.
1. Überprüfen Sie die Kategorieanforderung.
1. Optional: Wählen Sie auf dem Inforegister **Allgemein** im Feld **Grundcode** einen Grundcode aus. Geben Sie dann im Feld **Grundkommentar** einen Kommentar zu dem Grundcode ein.
1. Wählen Sie im Aktivitätsbereich **Workflow**.
1. Wählen Sie in den Workflow-Optionen **Genehmigen**.
1. Geben Sie im Feld **Kommentar** eine beliebige zusätzliche Information ein, die erforderlich ist. Wählen Sie dann **Genehmigen**, um die Anfrage abzuschließen.

    Der Status der Kategorieanforderung wird auf _Genehmigt_ geändert, und die Beschaffungskategorien werden dem Kreditor hinzugefügt.

### <a name="reject-a-pending-category-request"></a>Ablehnen einer ausstehenden Kategorieanfrage

Um eine ausstehende Kategorieanforderung abzulehnen, führen Sie diese Schritte aus.

1. Gehen Sie zu **Beschaffung und Bezugsquellenfindung \> Lieferanten \> Anfragen zur Zusammenarbeit mit Lieferanten \> Kategorie-Anfragen**.
1. Wählen Sie die ausstehende Anforderung, die Sie ablehnen möchten.
1. Überprüfen Sie die Kategorieanforderung.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie auf der Registerkarte **Allgemein** Inforegister, im Feld **Grundcode**, einen Grundcode aus. Geben Sie dann im Feld **Grundkommentar** einen Kommentar zu dem Grundcode ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktivitätsbereich **Workflow**.
1. Wählen Sie in den Workflow-Optionen **Mehr** und dann **Ablehnen**.
1. Geben Sie im Feld **Kommentar** eine beliebige zusätzliche Information ein, die erforderlich ist. Wählen Sie dann **Ablehnen**, um die Anfrage abzuschließen.

    Der Status der Kategorieanforderung wird auf _Abgelehnt_ geändert. An dieser Stelle kann der Lieferant bei Bedarf eine neue Kategorie-Anfrage erstellen.

### <a name="delegate-a-pending-category-request"></a>Delegieren einer ausstehenden Kategorieanforderung

Um eine ausstehende Kategorieanforderung an einen anderen Benutzer zu delegieren, führen Sie diese Schritte aus.

1. Gehen Sie zu **Beschaffung und Bezugsquellenfindung \> Lieferanten \> Anfragen zur Zusammenarbeit mit Lieferanten \> Kategorie-Anfragen**.
1. Wählen Sie den ausstehenden Auftrag, den Sie genehmigen wollen.
1. Wählen Sie im Aktivitätsbereich **Workflow**.
1. Wählen Sie in den Workflow-Optionen **Mehr** und dann **Delegieren**.
1. Wählen Sie im Feld **Benutzer** den Benutzer aus, dem die Kategorieanforderung zur Überprüfung zugewiesen werden soll.
1. Geben Sie im Feld **Kommentar** eine beliebige zusätzliche Information ein, die erforderlich ist.
1. Wählen Sie **Delegieren**, um die Delegation abzuschließen. Der ausgewählte Benutzer kann nun die Kategorieanforderung überprüfen.

### <a name="view-procurement-categories-for-a-vendor"></a>Beschaffungskategorien für einen Kreditor anzeigen

Um Beschaffungskategorien für einen Kreditor anzuzeigen, nachdem eine Kategorie-Anfrage genehmigt wurde, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Beschaffung \> Kreditoren \> Alle Kreditoren**.
1. Wählen Sie auf der Seite **Alle Kreditor** den Kreditor, für den Sie Beschaffungskategorien anzeigen möchten.
1. Öffnen Sie im Aktivitätsbereich die Registerkarte **Allgemein** und wählen Sie in der Gruppe **Einrichten** den Eintrag **Kategorien**.

    Die Seite **Kategorien** erscheint. Das Inforegister **Beschaffung** zeigt Beschaffungskategorien an, die über die Kategorieanforderung hinzugefügt wurden.

1. Auf der Registerkarte **Beschaffung** können Sie bei Bedarf Änderungen vornehmen. Sie können z.B. das Feld **Lieferantenkategoriestatus** auf _Bevorzugt_ festlegen.
