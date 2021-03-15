---
title: Übereinstimmung erstellen und verarbeiten
description: Dieses Thema erklärt, wie Sie die Qualitätsmangelverwaltung auf Basis eines vorhandenen Qualitätsprüfungsauftrags ausführen.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4525e79cb388cc9bbcfe1d038a53cf53916a678c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008075"
---
# <a name="create-and-process-a-conformance"></a>Übereinstimmung erstellen und verarbeiten

[!include [banner](../../includes/banner.md)]

Dieses Thema erklärt, wie Sie die Qualitätsmangelverwaltung auf Basis eines vorhandenen Qualitätsprüfungsauftrags ausführen. Sie können diese Buchung im USMF-Vorführungsunternehmen ausführen und können die vorgeschlagenen Werte verwenden. Normalerweise wird diese Prozedur aus einem Qualitätssekretär ausgeführt.  Als Voraussetzung müssen Sie die Anweisungen in [Qualität der Waren inspizieren](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) befolgen. Um die Genehmigung einer Nichtübereinstimmung zu verarbeiten, muss der Benutzer der das Aufgabenerfassen ausführt einen Wert Name besitzen, der auf der Benutzerseite zugewiesen ist. Um die Hinweisdokumente verwenden zu können, muss der Benutzer Handhabung von Dokumenten verfügen aktiviert in den Benutzeroptionen.


## <a name="select-a-quality-order"></a>Wählen Sie einen Qualitätsprüfungsauftrag aus.
1. Wechseln Sie im Navigationsbereich zu **Module > Lagerverwaltung > Periodische Aufgaben > Qualitätsmanagement > Qualitätsprüfungsaufträge**.
2. Wählen Sie in der Liste den Qualitätsprüfungsauftrag aus, der in [Qualität der Waren inspizieren](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) erstellt wurde.  

## <a name="create-a-nonconformance"></a>Erstellen einer Nichtübereinstimmung
1. Wählen Sie im Aktivitätsbereich **Abfragen** aus.
2. Wählen Sie **Nichtübereinstimmungen** aus.
3. Wählen Sie **Neu** aus.
4. Wählen Sie im Dropdownmenü des Feldes **Problemtyp**, das Problem aus, das während des Prüfprozesses gefunden wurde.  
5. Wählen Sie **OK**.

## <a name="approvereject-a-nonconformance"></a>Qualitätsmangeldatensätze genehmigen
1. Wählen Sie **Funktionen** aus.
2. Wählen Sie **Nichtübereinstimmung genehmigen** aus. In vorliegenden Beispiel genehmigen Sie den Qualitätsmangel. Genehmigte Qualitätsmängel können zugehörigen Arbeitsgängen zugeordnet werden, um Arbeit, die als Teil der Qualitätsmangelbehandlung ausgeführt wird, und, wie in diesem Thema, der Verarbeitung der Korrekturbehandlung, erfasst wird.  
3. Wählen Sie **Ja** aus.

## <a name="create-a-correction-action"></a>Korrektur erstellen
1. Wählen Sie **Veränderungen** aus.
2. Wählen Sie **Neu** aus.
3. Wählen Sie im Feld **Personalnummer** der neuen Zeile den gewünschten Datensatz aus dem Dropdownmenü aus.
4. Klicken Sie auf **Auswählen**.
5. Wählen Sie **Zuordnen** aus. Erstellen Sie einen Hinweis zur Korrektur. In vorliegenden Beispiel ist die Aktivität, mit dem Kreditor in Verbindung mit Ihnen aufzunehmen, um den Qualitätsmangelfall zu erläutern.  
6. Wählen Sie **Neu** aus.
7. Wählen Sie **Hinweis** aus. Abhängig von den Berichteinstellungen können verschiedene Dokumenttypen in den Berichten gedruckt werden, die der Qualitätsmangelverwaltung zugeordnet sind.  
8. Geben Sie im Feld **Beschreibung** einen Wert ein.
9. Schließen Sie die Seite.

## <a name="maintain-a-correction"></a>Korrekturen verwalten
1. Wählen Sie **Als abgeschlossen markieren** aus.
2. Wählen Sie **OK**.
3. Schließen Sie die Seite.

## <a name="close-a-nonconformance"></a>Qualitätsmangel schließen
1. Wählen Sie **Funktionen** aus.
2. Wählen Sie **Qualitätsmangel schließen** aus.
3. Wählen Sie **Ja** aus.
4. Schließen Sie die Seiten.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]