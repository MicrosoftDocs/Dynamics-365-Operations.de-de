---
title: Freitextrechnung erstellen
description: In diesem Artikel wird erläutert, wie Freitextrechnungen erstellt werden.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 87dc6334baa83ace23b77d94da4d1e464cb0b574
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878159"
---
# <a name="create-a-free-text-invoice"></a>Freitextrechnung erstellen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Freitextrechnungen erstellt werden. Für diese Prozedur wird das Demo-Unternehmen **USMF** verwendet.

## <a name="create-a-free-text-invoice"></a>Freitextrechnung erstellen

1. Rufen Sie **Debitoren (oder Verkaufssachkonto) \> Rechnungen \> Alle Freitextrechnungen** auf.
2. Wählen Sie **Neu** aus.
3. Wählen Sie im Feld **Debitorenkonto** einen Wert aus.

    * Das Rechnungskonto wird standardmäßig auf dasselbe Konto festgelegt, das für das Rechnungskonto verwendet wird.
    * Der Buchhaltungsstatus beginnt mit **In Bearbeitung**, wenn die Rechnung nicht gebucht wird.
    * Die Rechnungsnummer wird zugewiesen, wenn die Rechnung gebucht wird.
    * Wenn Sie einheitliche Euro-Zahlungsverkehrsraum-Vollmachten (SEPA) verwenden, wird das Direkteinzugsmandat automatisch mit einer Vollmacht aufgefüllt, wenn Sie das Debitorenkonto auswählen.

4. Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.
5. Geben Sie im Feld **Hauptkonto** eine Kontonummer ohne Dimensionen an. Sie geben Dimensionen weiter unten in diesem Artikel ein.

    Sie können auch ein oder mehrere Zeichen für das Hauptkonto eingeben und die Suche verwenden, um Ihr Konto zu suchen.

6. Erweitern Sie das Inforegister **Positionsdetails**, sodass Sie Ihrem Hauptkonto Dimensionen hinzufügen können.
7. Klicken Sie auf die Registerkarte **Finanzdimensionsposition**.

    * Die Dimensionen sind nur für die ausgewählte Position.
    * Die Mehrwertsteuergruppe wird standardmäßig aus dem Debitorendatensatz übernommen. Wenn der Debitor keine Mehrwertsteuergruppe aufweist, wird die Mehrwertsteuergruppe aus dem Hauptkonto verwendet.
    * Die Artikel-Mehrwertsteuergruppe wird vom Hauptkonto aufgefüllt. Wenn das Hauptkonto keine Artikel-Mehrwertsteuergruppe aufweist, wird die Artikel-Mehrwertsteuergruppe in den Mehrwertsteuerparametern für das Hauptbuch verwendet.

8. Optional: Geben Sie im Feld **Menge** eine Zahl ein.
9. Optional: Geben Sie im Feld **Einheitspreis** eine Zahl ein.

    Der Betrag wird als Menge mal Preis je Einheit berechnet. Sie können diese Berechnung jedoch außer Kraft setzen und einen Betrag eingeben.

10. Klicken Sie auf **Mehrwertsteuer**, um die Mehrwertsteuer anzuzeigen, die für Ihre Rechnung berechnet wird.

    Zeigen Sie die Mehrwertsteuerbeträge auf dieser Seite an oder Sie können die Beträge auf der Registerkarte **Regulierung** überschreiben.

11. Wählen Sie **OK**.
12. Klicken Sie auf **Belastungen**, um der Rechnung eine Belastung hinzuzufügen.
13. Geben Sie im Feld **Belastungen** einen Wert ein.
14. Geben Sie im Feld **Wert der Belastungen** eine Zahl ein.
15. Schließen Sie die Seite.
16. Klicken Sie auf **Summen**, um die zusammengefassten Rechnungsdetails und Summen anzuzeigen.
17. Wählen Sie **Schließen** aus.
18. Wählen Sie **Buchen** aus, um die Rechnung zu buchen. Sie haben noch eine Verkaufschance zu stornieren, bevor Sie buchen.

    * Sie können die Zeit des Rechnungsdruckes zu ändern. Wählen sie **Aktuell** um jede Rechnung zu drucken, wenn diese aktualisiert wird Wählen Sie **Später**, um alle Rechnungen zu drucken, die aktualisiert wurden.
    * Um zu ändern wie die Kreditlimite geprüft wird, bevor die Rechnung gebucht wird, ändern Sie den Wert im Feld **Kreditlimit-Typ**.
    * Sie können auswählen, dass die Freitext-Rechnungsbuchung gestoppt wird, wenn ein Fehler auf der **Aktualisierungen**-Registerkarte auf der **Debitorenparameter**-Seite (**Debitoren > Einrichtung > Debitorenparameter**) auftritt. Wähen Sie **Ja** für den Parameter **Buchung von Freitext-Rechnungen beim ersten Fehler stoppen**, um die Buchung von Freitextrechnungen zu stoppen, wenn ein Fehler auftritt. Wenn in einem Batch gebucht wird, stoppt ein Fehler den Buchungsprozess und der Batchstatus wird auf **Fehler** gesetzt. Wenn diese Option nicht ausgewählt ist, überspringt der Buchungsprozess eine Rechnung mit einem Buchungsfehler und bucht weitere Rechnungen weiter. Wenn Sie in einem Batch buchen, verhindert ein Buchungsfehler nicht, dass andere Rechnungen gebucht werden. Der Batchstatus lautet **Beendet**. Ein detaillierter Buchungsprozessbericht steht zur Überprüfung im Batchauftragsverlauf zur Verfügung.
    * Aktivieren Sie diese Option auf **Ja**, um die Rechnung zu drucken.
    * Aktivieren Sie diese Option auf **Ja**, um die Rechnung zu buchen. Sie können die Rechnung ohne Buchen drucken.

19. Wählen Sie **OK**.

## <a name="copy-lines"></a>Positionen kopieren
Um die Positionen auf der Freitextrechnung zu kopieren, wählen Sie eine oder mehrere Positionen aus und gehen anschließend auf **ausgewählte Positionen kopieren**. Sie können die Anzahl von Kopien angeben, die Sie erstellen möchten, und Sie können Hinweise und Anhänge kopieren. Sie können die Verteilungen kopieren oder zulassen, dass sie neu erstellt werden, wenn Sie buchen.

Anschließend können Sie die Informationen nach Bedarf bearbeiten.

## <a name="create-a-free-text-invoice-from-a-template"></a>Erstellen einer Vorlage für Freitext-Serienrechnungen
Sie können eine Freitext-Rechnung von einer Vorlage erstellen. Wenn Sie **Neu von Vorlage** aus der **Rechnungs** registerkarte auswählen, können Sie einen Vorlagennamen gür die neue Freitextrechnung auswählen. Sie können die Standardwerte wie die Zahlungsbedingungen und die Zahlungsmethode der Zahlung auch auswählen oder die Werte verwenden, , die mit der Vorlage gespeichert wurden.

Eine neue Freitextrechnung wird erstellt und Sie können die Werte in dieser Rechnung bearbeiten.

## <a name="resetting-the-workflow-status-for-free-text-invoices-from-unrecoverable-to-draft"></a>Zurücksetzen des Workflow-Status für Freitext-Rechnungen von Nicht wiederherstellbar auf Entwurf
Eine Workflowinstanz, die aufgrund eines nicht behebbaren Fehlers beendet wurde, hat ein Workflowstatus **Nicht behebbar**. Wenn der Status eines Workflows für Debitoren-Freitextrechnung **Nicht wiederherstellbar** ist, können Sie ihn auf **Entwurf** zurücksetzen, indem Sie **Rückruf** in den Workflowaktivitäten auswählen. Anschließend können Sie die Freitextrechnung des Debitoren bearbeiten. Diese Funktion ist verfügbar, wenn der Parameter **Zurücksetzen des Workflow-Status für Freitext-Rechnungen von „Nicht wiederherstellbar“ auf „Entwurf“** auf der Seite **Funktionsverwaltung** aktiviert ist.

Sie können die Seite **Workflowhistorie** verwenden, um den Workflowstatus auf **Entwurf** zurückzusetzen. Sie können diese Seite über **Freitextrechnung** oder **Allgemein > Abfragen > Workflow** öffnen. Um den Workflowstatus auf **Entwurf** zurückzusetzen, wählen Sie **Rückruf** aus. Sie können den Workflowstatus auch auf **Entwurf** zurücksetzen, indem Sie die Aktivität **Rückruf** auf der Seite **Freitextrechnung** oder **Alle Freitextrechnungen** auswählen. Nachdem der Workflowstatus auf **Entwurf** zurückgesetzt ist, wird er zur Bearbeitung auf der Seite **Freitextrechnung** verfügbar.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
