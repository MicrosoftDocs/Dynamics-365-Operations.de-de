---
title: "Übereinstimmung erstellen und verarbeiten"
description: "Verwenden Sie dieses Verfahren, um Qualitätsmangelverwaltung, auf Basis eines vorhandenen Qualitätsprüfungsauftrag auszuführen."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4082caf2cc8393345d4f79a991f2cf205b06b142
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-process-a-conformance"></a>Übereinstimmung erstellen und verarbeiten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Verwenden Sie dieses Verfahren, um Qualitätsmangelverwaltung, auf Basis eines vorhandenen Qualitätsprüfungsauftrag auszuführen. Sie können diese Buchung im USMF-Vorführungsunternehmen ausführen und können die vorgeschlagenen Werte verwenden. Normalerweise wird diese Prozedur aus einem Qualitätssekretär ausgeführt.  Als erforderliches folgenden Schaltern "überprüfen die Qualität von Waren" Aufgabenerfassen aus. Um die Genehmigung einer Nichtübereinstimmung zu verarbeiten, muss der Benutzer der das Aufgabenerfassen ausführt einen "Name Wert besitzen, der auf der Benutzerseite zugewiesen ist. Um die Hinweisdokumente verwenden zu können, muss der Benutzer Handhabung von Dokumenten verfügen aktiviert in den Benutzeroptionen.


## <a name="select-a-quality-order"></a>Wählen Sie einen Qualitätsprüfungsauftrag aus.
1. Qualitätsprüfungsaufträge (Formular) anzeigen
2. Markieren Sie in der Liste die ausgewählte Zeile.
    * Wählen Sie den Qualitätsprüfungsauftrag, der vom "überprüfen die Qualität von Waren" Aufgabenerfassen erstellt wurde.  

## <a name="create-a-nonconformance"></a>Erstellen einer Nichtübereinstimmung
1. Klicken Sie auf Abfragen.
2. Nichtübereinstimmungen klicken
3. Klicken Sie auf "Neu".
4. Klicken Sie im Feld "Problemtyp" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie das Problem aus, wenn während der Inspektionsprozesses gefunden wurde.  
5. Klicken Sie im Feld "Problemtyp" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie auf "OK".

## <a name="approvereject-a-nonconformance"></a>Qualitätsmangeldatensätze genehmigen
1. Klicken Sie auf Funktionen.
2. Die Nichtübereinstimmung genehmigen
    * In vorliegenden Beispiel genehmigen Sie den Qualitätsmangel. Genehmigte Qualitätsmängel können mit zugehörigen Arbeitsgängen zugeordnet werden, um Arbeit, die als Teil in der erfassenden zu erfassen Qualitätsmangelbehandlung und ausgeführt werden, wie in dieser Aufgabe, die Verarbeitung der Korrekturbehandlung.  
3. Klicken Sie auf "Ja".

## <a name="create-a-correction-action"></a>Korrektur erstellen
1. Korrekturen anklicken
2. Klicken Sie auf "Neu".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Klicken Sie im Feld "Personalnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie auf Auswählen.
7. Klicken Sie auf Anhänge.
    * Erstellen Sie einen Hinweis zur Korrektur. In vorliegenden Beispiel ist die Aktivität, mit dem Kreditor in Verbindung mit Ihnen aufzunehmen, um den Qualitätsmangelfall zu erläutern.  
8. Klicken Sie auf "Neu".
9. Klicken Sie auf Hinweis.
    * Beachten Sie, dass, abhängig von der Berichteinstellungen, verschiedene Dokumenttypen in den Berichten gedruckt werden können, die der Nichtübereinstimmung verwaltung zugeordnet sind.  
10. Geben Sie im Feld "Beschreibung" einen Wert ein.
11. Schließen Sie die Seite.

## <a name="maintain-a-correction"></a>Korrekturen verwalten
1. Klicken Sie auf "Abgeschlossen".
2. Klicken Sie auf "OK".
3. Schließen Sie die Seite.

## <a name="close-a-nonconformance"></a>Qualitätsmangel schließen
1. Klicken Sie auf Funktionen.
2. Qualitätsmangel schließen
3. Klicken Sie auf "Ja".
4. Schließen Sie die Seite.
5. Schließen Sie die Seite.

