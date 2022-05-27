---
title: Berichte zum Affordable Care Act in der Vorteilsverwaltung generieren
description: Dieses Thema beschreibt, wie das Benefits Management Informationen verfolgt, die auf den Formularen 1095-B und 1095-C für das Affordable Care Act (ACA) Arbeitgebermandat gemeldet werden.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 118dace557c7c8a8d101e2f2ad1d94fb14547c1b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688712"
---
# <a name="generate-aca-reports-in-benefits-management"></a>ACA-Berichte in der Vorteilsverwaltung generieren


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Das Benefits Management verfolgt Informationen, die auf den Formularen 1095-B und 1095-C für das Affordable Care Act (ACA)-Arbeitgebermandat gemeldet werden. Wie die ACA-Berichtsfunktion im alten **Vorteils**-Arbeitsbereich gilt diese Funktionalität nur für juristische Personen in den USA.

Um diese Funktionalität nutzen zu können, müssen Sie zuerst **Erweiterte Vorteilsverwaltung** aktivieren. Weitere Informationen, einschließlich wichtiger Vorbehalte zur Vorteilsverwaltung finden Sie unter [Aktivieren oder Deaktivieren der Vorteilsverwaltung](hr-admin-manage-features.md#enable-or-disable-benefits-management).

> [!IMPORTANT]
> Sie können ACA-Berichte nur entweder im Arbeitsbereich **Vorteilsverwaltung** oder im alten Arbetisbereich **Vorteile** verwenden, nicht in beiden. Wenn Sie beispielsweise zur Vorteilsverwaltung gewechselt sind, ist die ACA-Berichterstellung nur über Arbeitsbereich **Vorteilsverwaltung** verfügbar, nicht über den alten Arbeitsbereich **Vorteile**.
>
> Wenn Sie in der Mitte eines Beitrittsjahres zur Vorteilsverwaltung wechseln, müssen Sie die Mitarbeiterdaten für das gesamte Jahr korrekt in der Vorteilsverwaltung konfigurieren. Auf diese Weise stellen Sie sicher, dass Sie für das ganze Jahr genaue Berichtsinformationen erhalten.

## <a name="getting-started"></a>Erste Schritte

Um Informationen für 1095 Formulare zu verfolgen, erstellen Sie zunächst eine oder mehrere Dispositionssteuerungsgruppen für Affordable Care. Diese Gruppen geben die folgenden Informationen an:

- Das Angebot für Disposition, das einem Mitarbeiter zur Verfügung gestellt wurde
- Der Arbeitnehmeranteil an der niedrigsten monatlichen Prämie, wenn die Kosten über der Bundesarmutsgrenze liegen
- Der Safe Harbor, der gegebenenfalls vom Arbeitgeber genutzt wird

Mit Affordable Care-Dispositionssteuerungsgruppen können Sie diese Informationen für mehrere Mitarbeiterdatensätze mit denselben Bedingungen verwalten. Sie können einem oder mehreren Mitarbeitern problemlos Gruppen zuweisen.

### <a name="create-or-edit-an-affordable-care-coverage-group"></a>Erstellen oder bearbeiten Sie eine Affordable Care-Dispositionssteuerungsgruppe

1. Im **Vorteilsverwaltung**-Arbeitsbereich wählen Sie **Affordable Care-Dispositionssteuerungsgruppe**.

    ![Affordable Care-Dispositionssteuerungsgruppe auswählen.](./media/hr-benefits-management-aca-coverage-group.png)

2. Wählen Sie **Neu** aus, um eine neue Affordable Care-Dispositionssteuerungsgruppe zu erstellen, oder **Bearbeiten**, um eine vorhandene Gruppe zu ändern.

    ![„Neu“ oder „Bearbeiten“ auswählen.](./media/hr-benefits-management-aca-new.png)

3. Stellen Sie die folgenden Felder ein.

    | Feld | Beschreibung |
    |---|---|
    | Name | Geben Sie einen Namen für die Gruppe ein. |
    | Beschreibung | Geben Sie eine Beschreibung der Gruppe ein. |
    | Abdeckungsangebot | Die Disposition, die den Mitarbeitern, ihren Ehepartnern oder Partnern und ihren Unterhaltsberechtigten angeboten wird. |
    | Mitarbeiteranteil an den Kosten | Der Betrag, für den der Mitarbeiter zuständig ist. |
    | Gültiger Abschnitt 4980H in den Bestimmungen des amerikanischen Handelsministeriums (Safe Harbor) | Der Code für 4980H Safe Harbor oder Transition Relief. |
    | Startmonat des Vergütungsplans | Wählen Sie den Kalendermonat aus, an dem Ihr Vorteilsplan beginnt. |
    | Gruppe gültig ab | Das erste Datum, an dem dieser Datensatz gültig ist. |
    | Gruppe gültig bis | Das letzte Datum, an dem dieser Datensatz gültig ist. Wenn es kein Ablaufdatum gibt, geben Sie ein **Niemals** ein. |

    ![Erstellen einer Dispositionssteuerungsgruppe.](./media/hr-benefits-management-aca-new-group.png)

4. Wählen Sie **Speichern** aus.

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a>Einer Affordable Care-Dispositionssteuerungsgruppe mehrere Mitarbeiter zuweisen

1. Im **Vorteilsverwaltung**-Arbeitsbereich wählen Sie **Affordable Care-Dispositionssteuerungsgruppe**.
2. Wählen Sie die Gruppe aus, der Mitarbeiter zugewiesen werden sollen.
3. Wählen Sie **Massen-Zuweisung** aus.

    ![Massen-Zuweisung auswählen.](./media/hr-benefits-management-aca-mass-assignment.png)

4. Wählen Sie Mitarbeiter in der Liste aus und wählen Sie dann **Zuordnen**.

    ![Zuweisen der ausgewählten Mitarbeiter zu einer Gruppe.](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a>Mehrere Versionen von Dispositionsoptionen beibehalten

Sie können mehrere Versionen einer beliebigen Dispositionssteuerungsgruppe beibehalten. Wenn sich in Ihrer Organisation oder den angebotenen Vorteile etwas ändert, können Sie die Informationen der Gruppe auf dem neuesten Stand halten, ohne eine neue Gruppe erstellen und Mitarbeiter neu zuweisen zu müssen.

Nachdem Sie Affordable Care-Dispositionssteuerungsgruppen erstellt haben, können Sie ihnen durch Massen-Zuweisung Mitarbeiter zuweisen. Sie können Mitarbeiter auch einzeln Gruppen zuordnen und angeben, ob ACA-Informationen verfolgt und gemeldet werden.

Wenn Sie keine ACA-Informationen für einen Mitarbeiter verfolgen und melden müssen, können Sie die Option **Disposition melden** auf **Nein** festlegen. Beispielsweise haben Sie möglicherweise Teilzeitbeschäftigte, für die keine ACA-Berichterstattung erforderlich ist.

### <a name="override-default-values-for-an-employee"></a>Standardwerte für einen Mitarbeiter überschreiben

Für Mitarbeiter, die einer Affordable Care-Dispositionssteuerungsgruppe zugeordnet sind, können Sie die folgenden Optionen für alle Monate ändern, für die andere Werte erforderlich sind:

- Abdeckungsangebot
- Mitarbeiteranteil an den Kosten
- Gültiger Abschnitt 4980H in den Bestimmungen des amerikanischen Handelsministeriums (Safe Harbor)

> [!NOTE]
> Für ACA-Berichte aus dem Jahr 2020 müssen Sie auf dem Formular 1095-C sowohl die Postleitzahl der Arbeitsstelle als auch die für Zuhause angeben. Die Werte werden basierend auf den aktuell aktiven Standorten automatisch eingegeben. Wenn einer der Standorte während eines Teils des Jahres anders war, müssen Sie den Wert überschreiben. Das **Postleitzahl**-Feld (Zeile 17) des 1095-C-Berichts wird nur ausgefüllt, wenn der Code **Angebot für Disposition** wie folgt **1L** bis **1Q** enthält:
>
> - **1L, 1M oder 1N:** Die Postleitzahl des Hauptwohnsitzes
> - **1O, 1P, 1Q:** Die Postleitzahl des Hauptarbeitsplatzes

Führen Sie die folgenden Schritte aus, um Ausnahmen für Werte einer Affordable Care-Dispositionssteuerungsgruppe einzugeben.

1. Wählen Sie im Arbeitsbereich **Personalverwaltung** **Links** und dann **Arbeitskräfte** aus.
2. Wählen Sie den Mitarbeiter in der Liste aus.
3. Auf der **Beschäftigung**-Registerkarte im **Mehr Informationen**-Abschnitt wählen Sie **Affordable Care-Dispositionssteuerungsgruppe**.

    ![Optionen für einen Mitarbeiter ändern.](./media/hr-benefits-management-aca-change-single-employee.png)

4. Wählen Sie **Bearbeiten** aus.
5. Aktivieren Sie für jeden Monat, für den Änderungen erforderlich sind, das Kontrollkästchen **Standard überschreiben** und ändern Sie die anderen Werte nach Bedarf.

    ![Standardwerte überschreiben.](./media/hr-benefits-management-aca-override-default.png)

6. Wählen Sie **Speichern** aus.

## <a name="report-health-care-coverage"></a>Gesundheitsvorsorgedisposition melden

Sie müssen alle vom Arbeitgeber unterstützten, selbstversicherten Krankenversicherungen für Vollzeit- und Teilzeitbeschäftigte nachverfolgen. Nehmen Sie jeden Mitarbeiter zusammen mit seinen Unterhaltsberechtigten in den 1095-C-Bericht für die Monate auf, in denen er versichert war.

Befolgen Sie diese Schritte, um anzugeben, ob ein Vorteilsplan gemeldet werden muss.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** die Option **Vorteilspläne** aus.
2. Wählen Sie den zu meldenden Vorteilsplan aus.
3. Wählen Sie **Bearbeiten** aus.
4. Legen Sie die Option **Gemäß Affordable Care Act gemeldet** auf **Ja** fest.

    ![Melden von Gesundheitsvorsorgeabdeckung.](./media/hr-benefits-management-aca-report-coverage.png)

5. Wählen Sie **Speichern** aus.

Wenn ein Mitarbeiter eine Krankenversicherung für einen Unterhaltsberechtigten wählt, wird der Versicherungszeitraum des Unterhaltsberechtigten durch das Datum bestimmt, an dem der Unterhaltsberechtigte registriert oder entfernt wurde. Die Dispositionstermine für Unterhaltsberechtigte werden automatisch auf der Grundlage des Zeitraums berechnet, in dem der Unterhaltsberechtigte während des Registrierungsjahres berechtigt und in einem Plan aktiv war.

## <a name="generate-1095-b-and-1095-c-forms"></a>1095-B- und 1095-C-Formulare generieren

Sie können ACA-Formulare 1095-B und 1095-C generieren und dann an jeden der Mitarbeiter verteilen. Sie können das Formular 1095-C und die entsprechenden 1094-C-Übermittlungsdateien auch elektronisch generieren, um sie an den Internal Revenue Service (IRS) zu senden.

1. Im Arbeitsbereich **Vorteilsverwaltung** wählen Sie **ACA-Formular 1095-B** oder **ACA-Formular 1095-C**.
2. Ändern Sie die Parameter nach Bedarf und wählen Sie dann **OK**.

    > [!NOTE]
    > Wenn Sie 1095-C Formulare für mehr als 500 Mitarbeiter drucken, erhalten Sie mehr als eine PDF-Datei. Wir empfehlen Ihnen, den Wert des Felds **Maximale Dateigröße in Megabyte** auf der Seite **Parameter für die Dokumentenverwaltung** auf **150** zu erhöhen. (Um diese Seite schnell zu öffnen, verwenden Sie das Suchfeld in der Navigationsleiste).
    >
    > ![Ändern der maximalen Dateigröße.](./media/hr-benefits-management-aca-maximum-file-size.png)

3. Verwenden Sie das Suchfeld in der Navigationsleiste, um den Status Ihrer Berichte zu überprüfen und anzuzeigen und die Seite **Elektronische Berichterstattung** zu öffnen.

    ![Suchen nach der Seite „Elektronische Berichterstattung“.](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. Wählen Sie den anzuzeigenden Bericht aus und wählen Sie dann **Dateien anzeigen**.

    ![Anzeigen von Dateien.](./media/hr-benefits-management-aca-show-files.png)

5. Wählen Sie **Öffnen**.

    ![Öffnen einer Datei.](./media/hr-benefits-management-aca-open-file.png)

6. Öffnen Sie in der Benachrichtigungsleiste am unteren Rand des Browserfensters die Zip-Datei und wählen Sie den Bericht aus. Sie können die PDF-Datei anzeigen oder drucken.

    ![1095-C-Beispielformular.](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a>Informationen zur ACA-Disposition anzeigen

Die Seite **Disposition für Affordable Care Act für Arbeitskraft** zeigt die folgenden Informationen:

- Mitarbeiter, die jeder Dispositionssteuerungsgruppe zugewiesen sind
- Mitarbeiter, die nicht in einen Bericht aufgenommen werden müssen
- Nicht zugewiesene Mitarbeiter

Führen Sie die folgenden Schritte aus, um diese Informationen anzuzeigen.

1. Im **Vorteilsverwaltung**-Arbeitsbereich wählen Sie **Disposition für Affordable Care Act für Arbeitskraft**.
2. Wählen Sie im Feld **Gruppenname** eine Gruppe aus.

    ![Anzeigen der ACA-Disposition.](./media/hr-benefits-management-aca-view-coverage.png)

Wenn beliebige Standardwerte der Affordable Care-Dispositionssteuerungsgruppe überschrieben wurden, wird ein Sternchen neben dem geänderten Wert angezeigt. Wenn die Werte für alle 12 Monate identisch sind und nicht überschrieben wurden, wird der Wert in der Spalte **Alle 12 Monate** angezeigt.

Sie können Mitarbeiter anzeigen, die als nicht ACA-meldepflichtig markiert sind und für die kein 1095-C-Formular erforderlich ist. Im Feld **Filtern nach** wählen Sie **Nicht ACA-meldepflichtig** aus.

Sie können Mitarbeiter anzeigen, die keiner Gruppe oder einer abgelaufenen Gruppe zugeordnet sind. Im Feld **Filtern nach** wählen Sie **Nicht zugewiesene oder abgelaufene Gruppe** aus.

### <a name="export-to-excel"></a>Nach Excel exportieren

Befolgen Sie diesen Schritten, um eine der Listen nach Microsoft Excel zu exportieren.

1. Wählen Sie die Schaltfläche **In Microsoft Office öffnen** aus.
2. Wählen Sie **Zeitweise HCM-Personalwesentabelle für internen Gebrauch**.
3. Wählen Sie **Herunterladen**.

### <a name="view-aca-reportable-dependents"></a>ACA-meldepflichtige Unterhaltsberechtigte anzeigen

Wenn Sie versicherte Personen melden müssen, weil Sie selbstversicherten Versicherungsschutz bieten, können Sie Unterhaltsberechtigte anzeigen, die im Rahmen von Vorteilsplänen versichert sind, die als **ACA-meldepflichtig** gekennzeichnet sind. Wählen Sie im Aktionsbereich **Disposition für Unterhaltsberechtigte anzeigen** aus.

![Anzeigen der Disposition für Unterhaltsberechtigte.](./media/hr-benefits-management-aca-view-dependent-coverage.png)

Dispositionsinformationen für Unterhaltsberechtigte des Mitarbeiters werden angezeigt.

![Deckung für Unterhaltsberechtigte.](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> Auf der Seite werden nur Vorteilspläne angezeigt, die als **ACA-meldepflichtig** gekennzeichnet sind.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
