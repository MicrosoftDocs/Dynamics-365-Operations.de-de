---
title: Produktionsauftrag erstellen
description: Diese Prozedur zeigt, wie ein Produktionsauftrag erstellt wird.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute, ProdJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ce08532b8281d730cd5fae4ebd634a08c5baeedd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428418"
---
# <a name="create-a-production-order"></a>Produktionsauftrag erstellen

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie ein Produktionsauftrag erstellt wird. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Dies ist die erste Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.


## <a name="create-a-production-order"></a>Produktionsauftrag erstellen
1. Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".
2. Klicken Sie auf "Neuer Produktionsauftrag".
3. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "D0001" ein.
4. Geben Sie im Feld "Lieferung" ein Datum ein.
    * Das Lieferdatum zeigt an, wann der Produktionsauftrag enden soll, um pünktlich zu liefern. Dieses Datum kann im Planungsprozess verwendet werden. Sie können beispielsweise den Auftrag rückwärts ab dem Lieferdatum planen.  
5. Legen Sie die Menge auf "20" fest.
    * Hinweis: Das Feld "Stücklistennummer" zeigt automatisch die Nummer von jeder aktiven Stücklisten für den aktuellen Artikel an, aber Sie können die Stückliste für den Produktionsauftrag ändern, indem Sie eine aktive Stückliste aus der Liste der genehmigten Stücklistenversionen auswählen.    Das Feld "Arbeitsplannummer" zeigt automatisch die Nummer von jeder aktiven Stücklisten für den aktuellen Artikel an, aber Sie können den Arbeitsplan für den Produktionsauftrag ändern, indem Sie einen aktiven Arbeitsplan aus der Liste der genehmigten Arbeitsplanversionen auswählen.  
6. Klicken Sie auf "Erstellen".

## <a name="validate-the-production-order"></a>Den Produktionsauftrag überprüfen
1. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Klicken Sie auf den Link für die Produktionsauftragsnummer, die Sie soeben erstellt haben. Dadurch wird die Detailseite für den Auftrag geöffnet.  
2. Klicken Sie auf "Bearbeiten".
3. Geben Sie im Feld "Lieferung" ein Datum ein.
    * Sie können beispielsweise das Lieferdatum für den Produktionsauftrag ändern.  
4. Klicken Sie auf "Speichern".
5. Schließen Sie die Seite.

## <a name="update-the-bom"></a>Die Stückliste aktualisieren
1. Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".
2. Klicken Sie auf "Stückliste".
    * Öffnen Sie die Stücklistenseite, um die Stücklistendaten zu prüfen, die von den Standarddaten kopiert wurden, als der Produktionsauftrag erstellt wurde. In dieser Prozedur müssen Sie die Menge für eine Stückliste aktualisieren.  
3. Klicken Sie auf "Bearbeiten".
4. Geben Sie im Feld "Menge" eine Zahl ein.
    * Das Ändern der Menge in der Stücklistenposition wirkt sich auf die Vorkalkulation des Materialverbrauchs für den Produktionsauftrag aus.  
5. Klicken Sie auf "Speichern".
6. Schließen Sie die Seite.

## <a name="update-the-production-route"></a>Den Produktionsarbeitsplan aktualisieren
1. Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".
2. Klicken Sie auf "Arbeitsplan".
    * Öffnen Sie die Arbeitsplanseite, um die Daten des Produktionsarbeitsplans zu prüfen, die von den Standarddaten kopiert wurden, als der Auftrag erstellt wurde. In dieser Prozedur müssen Sie die Menge für einen der Arbeitsgänge im Produktionsarbeitsplan aktualisieren.  
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie auf "Bearbeiten".
5. Geben Sie im Feld Prozessmenge eine Zahl ein.
    * Das Ändern der Bearbeitungszeit wirkt sich auf die geschätzte Arbeitsplanrückmeldung und die Kosten des Produktionsauftrags aus.  
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.

