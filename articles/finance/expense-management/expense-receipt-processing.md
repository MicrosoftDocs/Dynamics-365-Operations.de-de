---
title: Ausgabenbelegverarbeitung
description: Dieses Thema enthält Informationen zur optischen Zeichenerkennung (OCR) für Belege. Diese Funktion wurde entwickelt, um die Benutzerfreundlichkeit bei der Erstellung von Spesenabrechnungen in Microsoft Dynamics 365 Finance zu verbessern.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2e819521828b054f70476b1eb061ee08c486d09f
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113685"
---
# <a name="public-preview-expense-receipt-processing"></a>Öffentliche Vorschau: Verarbeitung von Ausgabenbelegen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Die Ausgabenerfassung wurde durch die Einführung der OCR-Verarbeitung für Belege erweitert. Diese Funktion wurde entwickelt, um die Benutzerfreundlichkeit bei der Erstellung von Spesenabrechnungen zu verbessern.

## <a name="key-features"></a>Schlüsselfeatures

- Der Händlername, das Datum und der Gesamtbetrag werden aus den Belegen extrahiert.
- Die Funktion versucht, nicht angehängte Belege mit nicht angehängten Ausgabenbuchungen abzugleichen.
- Benutzer können manuell eingegebene Ausgabenbuchungen aus Belegen erstellen.

## <a name="usage-examples"></a>Anwendungsbeispiele

- **Belege mit Kreditkartenbuchungen automatisch anhängen, wenn ein Spesenbericht erstellt wird.**

    1. Öffnen Sie den Arbeitsbereich **Ausgabenverwaltung**.
    2. Überprüfen Sie auf der Registerkarte für **Belege**, ob nicht angehängte Belege vorhanden sind. Sie können Belege auch auf die Registerkarte **Belege** hochladen.
    3. Überprüfen Sie auf der Registerkarte **Ausgaben**, ob nicht angehängte Ausgaben vorhanden sind. In der Regel importiert der Ausgabenadministrator diese Ausgaben vom Kreditkartenanbieter.
    4. Wählen Sie **Neue Spesenabrechnung**. Beachten Sie, dass Sie beim Erstellen einer Spesenabrechnung jetzt auch Ausgaben und Belege einschließen können. Wenn Sie sowohl Ausgaben als auch Belege hinzufügen, wird ein automatischer Abgleich der Belege mit den Ausgaben durchgeführt.

- **Erstellen einer Ausgabe oder Abgleichen einer Ausgabe aus einem Beleg.**

    1. Fügen Sie bei einer Spesenabrechnung auf der Registerkarte **Belege** einen Beleg hinzu, indem Sie **Belege hinzufügen** auswählen.
    2. Beachten Sie unter dem hochgeladenen Bild des Belegs die Optionen **Erstellen** und **Abgleichen**.

        - Wählen Sie **Erstellen** aus, um eine manuell eingegebene Ausgabenbuchung zu erstellen, und geben Sie die aus dem Beleg extrahierten Werte ein.
        - Wenn Sie **Abgleichen** auswählen, versucht das System, dem Beleg eine vorhandene Ausgabe zuzuordnen.

## <a name="installation"></a>Installation

Diese Funktion funktioniert in Kombination mit der Funktion **Spesenabrechnungen neu gestaltet**, um die Erfahrung mit der Ausgabenverarbeitung zu verbessern.

Wenn Sie diese erweiterten Ausgabenfunktionen nutzen möchten, installieren Sie das Add-In für den Spesenverwaltungsdienst für Microsoft Dynamics 365 Finance und aktivieren Sie die Funktionen in Ihrer Instance. Sie können auf das Add-In über Ihr Projekt in Microsoft Dynamics Lifecycle Services (LCS) zugreifen.

1. Melden Sie sich bei LCS an und öffnen Sie die gewünschte Umgebung.
2. Gehen Sie zu **Vollständige Details**.
3. Wählen Sie **Beibehalten**, oder scrollen Sie nach unten zu den **Umgebungs-Add-Ins** Inforegister.
4. Wählen Sie **Installieren Sie ein neues Add-In**.
5. Wählen Sie **Spesenverwaltungsdienst** aus.
6. Befolgen Sie die Installationsanleitung und erklären Sie sich mit den Allgemeinen Geschäftsbedingungen einverstanden.
7. Wählen Sie **Installieren**.

Aktivieren Sie im Arbeitsbereich **Funktionsverwaltung** die folgenden Funktionen:

- Spesenabrechnungen neu gestaltet
- Automatisch abgleichen und Ausgaben aus Beleg erstellen

Wenn Sie diese Funktionen aktivieren, werden die folgenden Aktivitäten ausgeführt:

- Der vorhandene Arbeitsbereich **Ausgabenverwaltung** wird durch den neuen ersetzt.
- Ein neues Menüelement für Ausgabenenfeldsichtbarkeit wird hinzugefügt.
- Sie können weiterhin die vorherige Seite **Spesenabrechnungen** aufrufen, indem Sie zu **Ausgabenverwaltung > Meine Ausgaben > Spesenabrechnungen** navigieren.
- Abläufe und alle Genehmigungen führen Sie weiterhin zur bestehenden Ausgabenberichtsseite.
- Belege werden durch die Microsoft Azure Cognitive Services verarbeitet und Metadaten werden extrahiert und hinzugefügt.
- Es wird eine Option hinzugefügt, mit der Sie eine Spesenabrechnung erstellen können, die übereinstimmende nicht angehängte Belege enthält.
- Mit einer Option, die zu den Spesenabrechnungen hinzugefügt wurde, können Sie eine Ausgabenzeile aus einem Beleg erstellen oder einen vorhandenen Beleg mit einer vorhandenen Ausgabenzeile abgleichen.

Weitere Informationen zur Funktion „Spesenabrechnungen neu gestaltet“ finden Sie unter [Spesenabrechnungen neu gestaltet](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Verwendet Microsoft meine Daten für seine Modelle?**

Nein, Microsoft hat ein allgemeines Machine Learning-Modell für seinen Dienst zur Belegverarbeitung. Dieses Modell basiert nicht auf den von Ihnen hochgeladenen Belegen.

**Wo ist diese Funktion verfügbar und wo wird sie verarbeitet?**

Derzeit wird diese für die USA unterstützt.

**Wohin gehen meine Belege?**

Finance wird sich mit Cognitive Services in Verbindung setzen, um die Felddaten zu extrahieren. Cognitive Services bewahrt eine Kopie Ihres Belegs bis zu 24 Stunden lang auf, während die Verarbeitung erfolgt. Nach Abschluss der Verarbeitung entfernt Cognitive Services den Beleg. Belege werden weiterhin in Finance gespeichert.

Weitere Informationen finden Sie unter [Ermöglichen des Verstehens von Belegen mit der neuen Funktion der Formularerkennung das Verstehen von Belegen](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
