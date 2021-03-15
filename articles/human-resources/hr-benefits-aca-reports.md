---
title: Erstellen von Affordable Care Act-(ACA)-Berichten
description: Die Berichterstattung nach dem Affordable Care Act (ACA) generiert die Formulare 1095-B und 1095-C zur Unterstützung des Teils **Arbeitgebermandat** des Affordable Care Act.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 56ff879603a31956db877b45aec11b15371b69f5
ms.sourcegitcommit: 5c1b5ef40ce7359b3f1955535a250718d863badb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "5142155"
---
# <a name="generate-aca-reports"></a>ACA-Berichte generieren

Die Berichterstattung nach dem Affordable Care Act (ACA) generiert die Formulare 1095-B und 1095-C zur Unterstützung des Teils **Arbeitgebermandat** des Affordable Care Act.

> [!NOTE]
> Die ACA-Berichterstattung ist nur für juristische Personen in den USA aktiviert.

## <a name="getting-started"></a>Erste Schritte

Um Informationen für die Formulare 1095-B und 1095-C zu verfolgen, müssen Sie zunächst eine oder mehrere Dispositionssteuerungsgruppen für Affordable Care erstellen. Affordable Care-Dispositionssteuerungsgruppe geben Folgendes an:

- Das Dispositionsangebot für einen Mitarbeiter
- Der Arbeitnehmeranteil an der niedrigsten monatlichen Prämie, wenn die Kosten über der Bundesarmutsgrenze liegen
- Safe Harbor, der gegebenenfalls vom Arbeitgeber genutzt wird

Mit Affordable Care Act-Gruppen können Sie die Informationen für diese Felder zu verwalten, ohne alle Mitarbeiterdatensätze mit gleichen Bedingungen ändern zu müssen. Sie können leicht Affordable Care-Dispositionssteuerungsgruppen mit der Option **Massenzuweisung** auf der Seite einem oder mehreren Mitarbeitern zuweisen.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Mehrere Versionen einer Dispositionssteuerungsgruppe aufrecht halten

Sie können mehrere Versionen einer beliebigen Dispositionssteuerungsgruppe beibehalten. Mit dieser Funktion können Sie Änderungen vornehmen, ohne eine neue Gruppe erstellen und Mitarbeiter neu zuweisen zu müssen. 

Nachdem Sie ACA-Dispositionssteuergruppen erstellt haben, können Sie die Gruppen massenhaft Mitarbeitern mit der Option **Massenzuweisung** zuweisen. Sie können auch individuell angeben, ob ACA-Informationen nachverfolgt und gemeldet werden sollen, und einen Mitarbeiter einer Affordable Care-Dispositionssteuergruppe zuordnen.

Sie müssen einige Informationen zur ACA-Disposition nicht nachverfolgen, z. B. für Teilzeitbeschäftigte. Stellen Sie in diesem Fall das Feld **Berichterstattung melden** auf **Nein**. Obwohl Sie jeden Mitarbeiter mit nachverfolgbaren ACA-Informationen einer Affordable Care-Dispositionssteuerungsgruppe zuordnen müssen, können Sie die folgenden Optionen für Monate mit unterschiedlichen Werten ändern:

- **Abdeckungsangebot**
- **Mitarbeiteranteil an den Kosten**
- **Safe Harbor**

Um Ausnahmen für Affordable Care-Dispositionssteuerungsgruppenwerte einzugeben, wählen Sie den Link **Affordable Care-Disposition** auf der Seite **Details zur Arbeitskraft**, unter dem Abschnitt **Zusätzliche Informationen** auf der Registerkarte **Mitarbeiter**.

## <a name="reporting-health-care-coverage"></a>Melden von Gesundheitsvorsorgeabdeckung

Neben der Nachverfolgung, ob Vollzeitmitarbeitern Krankenversicherungsschutz angeboten wird, ob der Arbeitgeber eine vom Arbeitgeber geförderten selbstversicherten Krankenversicherungsschutz, für den der Mitarbeiter registriert ist, (unabhängig davon, ob sie Vollzeit- oder Teilzeitbeschäftigt sind) anbietet, müssen Zusatzinformationen im 1095-C gemeldet werden. Jeder Mitarbeiter (einschließlich abhängiger), die von Arbeitgeber-geförderten Vorteilspläne abgedeckt sind, muss in dem Bericht für die Monate einbezogen werden, die sie abgedeckt waren. 

Sie können angeben, ob jeder Vorteilsplan angegeben werden muss, indem Sie das Kontrollkästchen **ACA meldepflichtig** aktivieren.

Wenn Mitarbeiter darüber hinaus ausgewählt haben, irgendwelche ihrer abhängigen Personen unter einem Vorteil abdecken zu lassen, können Sie auf der Seite **Vorteile verwalten** das Datum angeben, zu dem die Unterhaltsberechtigten für jeden Mitarbeiter abgedeckt wurden. Um anzugeben dass der Unterhaltsberechtigte unter dem Vorteil abgedeckt wird, wählen Sie im Aktivitätsbereich des Inforegisters **Unterhaltsberechtigte** die Schaltfläche **Bearbeiten** aus.

Auf der Seite **Manager des Dispositionsdatums für Unterhaltsberechtigte** können Sie den Zeitraum angeben, zu dem der Unterhaltsberechtigte durch die Vergütung abgedeckt wurde. Das Eingeben von Daten auf dieser Seite aktiviert automatisch das Kontrollkästchen **Abgedeckt** auf der Seite **Vergütungen verwalten**.

## <a name="generate-1095-b-and-1095-c-forms"></a>1095-B- und 1095-C-Formulare generieren

Sie können Formulare 1095-B und mit 1095-C im Produkt erstellen und sie an jeden der Mitarbeiter verteilen. Das System kann auch elektronisch 1095-C-Formulare und die 1094-C-IRS-Übertragungsdateien generieren.  

Wenn Sie das Formular 1095-C generieren, geben Sie das jeweilige Geschäftsjahr ein und geben Sie an, ob Sozialversicherungsnummern maskiert werden. Wenn Sie 1095-C Formulare für mehr als 500 Mitarbeiter drucken, erhalten Sie mehr als eine PDF-Datei. Es wird empfohlen, dass Sie **Maximale Dateigröße** im Fenster **Parameter der Dokumentverwaltung** auf 150 MB erhöhen.

## <a name="viewing-information"></a>Informationen anzeigen

Sie können die Seite **Deckung für Affordable Care Act für Arbeitskraft** verwenden, um festzustellen, welche Mitarbeiter jeder Dispositionssteuerungsgruppe zugewiesen wurden, welche Mitarbeiter im Bericht nicht eingeschlossen werden müssen und welche Mitarbeiter nicht zugewiesen sind.

Wurden irgendwelche der Standardwerte der Affordable Care-Dispositionssteuerungsgruppe überschrieben, wird ein Sternchen neben dem geänderten Wert angezeigt. Wenn die Werte für alle 12 Monate identisch sind und nicht überschrieben wurden, wird der Wert in der Spalte **Alle 12 Monate** ausgegeben.

Sie können auch das Anfragefenster verwenden, um zu verstehen, welche Mitarbeiter als nicht ACA-meldepflichtig gekennzeichnet wurden. Sie müssen nicht nachverfolgen, ob ihnen Versicherungsschutz angeboten wurde, und müssen ihnen Ende des Jahres keinen 1095-C ausstellen. Wählen Sie **Nicht ACA meldepflichtig** im Feld **Filtern nach** aus, um eine Liste aller Mitarbeiter zu erstellen, die keinen 1095-C erhalten.

Zusätzlich können Sie alle Mitarbeiter anzeigen, die nicht zugewiesen sind (das Feld **ACA-Berichtsdisposition** ist leer) oder die einer Affordable Care-Dispositionssteuerungsgruppe zugewiesen wurden, die für das im Feld **Jahr** ausgewählte Jahr abgelaufen ist.

Sie können Mitarbeiterlisten exportieren, die mithilfe einer der Filteroptionen in Excel generiert wurden.

Wenn Sie versicherte Personen melden müssen, weil Sie selbstversicherten Versicherungsschutz bieten, können Sie Unterhaltsberechtigte anzeigen, die im Rahmen von Vorteilsplänen versichert sind, die als **ACA-meldepflichtig** gekennzeichnet sind. Wählen Sie im Aktionsbereich **Disposition für Unterhaltsberechtigte anzeigen** aus.

> [!NOTE]
> Nur Vorteilspläne, die als **ACA-meldepflichtig** gekennzeichnet sind, werden im Anfragefenster angezeigt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]