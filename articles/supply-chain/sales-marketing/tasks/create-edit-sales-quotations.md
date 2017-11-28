--- 
title: Verkaufsangebote erstellen und bearbeiten
description: Diese Verfahren zeigt, wie ein Verkaufsangebot erstellt und aktualisiert wird.
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: 7ffa4fe8d87db5b3f8293ec9dbc042496d09d6e3
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---
# <a name="create-and-edit-sales-quotations"></a>Verkaufsangebote erstellen und bearbeiten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Verfahren zeigt, wie ein Verkaufsangebot erstellt und aktualisiert wird. Sie können diese Prozedur in Ihrem eigenen Demodatenunternehmen oder in USMF ausführen.


## <a name="create-a-sales-quotation"></a>Ein Verkaufsangebot erstellen
1. Wechseln Sie zu "Vertrieb und Marketing" > "Verkaufsangebote" > "Alle Angebote".
2. Klicken Sie auf "Neu".
3. Wählen Sie im Feld "Kontotyp" "Interessent" aus.
4. Geben Sie im Feld '"Interessent' einen Wert ein, oder wählen Sie einen Wert aus.
5. Erweitern Sie den Abschnitt "Allgemein".
    * Da Sie sich für die Erstellung eines Angebots über den Bereich "Vertrieb und Marketing" entschieden haben, wird der Typ automatisch auf Verkaufsangebot festgelegt. Um ein Angebot für ein Projekt zu erstellen, müssen Sie über das Projektverwaltungs- und Buchhaltungsmodul zugreifen.   
6. Klicken Sie auf "OK".
    * Die Felder und Aktivitäten der Angebotspositionen sind mit denen in den Auftragspositionen vergleichbar.   Wie Aufträge können auch Angebote für einen bestimmten Artikel erstellt werden. Wenn Artikelnummer nicht bekannt ist oder nicht zum Zeitpunkt der Erstellung Angebots vorhanden ist, können Angebote für eine Verkaufskategorie erstellt werden.  
7. Geben Sie im Feld 'Artikel' einen Wert ein, oder wählen Sie einen Wert aus.
8. Geben Sie im Feld "Artikel einen Wert ein.
9. Schließen Sie die Seite.
10. Geben Sie im Feld "Menge" eine Zahl ein.
    * Sind gültige Handelsvereinbarungen für den zur Position ausgewählten Artikel vorhanden, werden die entsprechenden Preise und Rabatte automatisch in die Angebotsposition kopiert. Stellen Sie sicher, dass das Feld "Preis je Einheit" einen Wert enthält. Sie können auch Rabattwerte eingeben.  
11. Klicken Sie auf "Speichern".
12. Klicken Sie im Aktivitätsbereich auf "Verkaufsangebot".
13. Klicken Sie auf "Summen".
14. Klicken Sie auf "OK".
15. Klicken Sie auf "Verkaufsangebotsposition".
16. Klicken Sie auf "Preise".
    * In der Seite "Ausführungspreissimulation" können Sie mit der Anpassung des erwarteten Umsatzerlöses oder der Rentabilität des Angebots auf Grundlage des gewünschten "Preis je Einheit", des Rabattbetrags, des Rabattprozentsatzes, des Gesamtbetrags, der Gewinnspanne bzw. des Deckungsbeitrags experimentieren.   Wenn Sie mit den Zielvorgaben zufrieden sind, wenden Sie den Vorschlag auf die Angebotsposition an und die preisbezogene Felder werden entsprechend aktualisiert.  
    * Sie können so viele Preissimulationen erstellen wie gewünscht. Wenn Sie auf "Neu" klicken, werden die Preisbedingungen von der aktuellen Angebotsposition zur Seite kopiert. Sie können die Werte in jedem der preisbezogene Felder auf die Zielwerte ändern. Eine Änderung in einem der Felder löst eine Neuberechnung für alle anderen Felder aus. Damit das System die Handelsspanne und den Deckungsbeitrag berechnen kann, müssen die Einheitenkosten des Produkts muss bekannt sein. Verwenden Sie Registerkarte "Simulierte Preise" für eine detaillierte Ansicht der ursprünglichen Preise, der vorgeschlagenen Änderungen und ihrer Auswirkungen auf den Angebotssummen.   Wenn eine Simulation für einen neuen Betrag auf ein Angebot angewendet wird, berechnet das System neu und legt einen neuen Wert für das Feld Preis je Einheit" fest. Wenn die Simulation auf Grundlage eines neuen Deckungsbeitrags oder ein neues Deckungsbeitragsverhältnis basiert, wird nur das Feld "Nettobetrag" aktualisiert. Der Preis je Einheit ist leer. In beiden Fällen werden alle Rabatten für die Angebotsposition gelöscht.  
17. Schließen Sie die Seite.
18. Klicken Sie im Aktivitätsbereich auf "Angebot".
19. Klicken Sie auf "Angebot versenden".
20. Wählen Sie "Ja" im Feld "Angebot drucken" aus.
21. Klicken Sie auf "OK".
    * Der Bericht kann einige Minute dauern. Schließen Sie nicht die Seite.  
22. Schließen Sie die Seite.

## <a name="update-a-sales-quotation"></a>Ein Verkaufsangebot aktualisieren
1. Klicken Sie im Aktivitätsbereich auf "Nachverfolgung".
2. Klicken Sie auf "In Debitor konvertieren".
3. Geben Sie im Feld "Kundenkonto" einen Wert ein.
4. Klicken Sie auf "Prüfen".
    * Stellen Sie sicher, das eine Nachricht anzeigt, dass die Kontonummer frei ist.  
5. Klicken Sie auf "OK".
    * Das System hat nun ein neues Debitorenkonto für den Interessenten im Angebot erstellt.  
6. Schließen Sie die Seite.
7. Klicken Sie im Aktivitätsbereich auf "Nachverfolgung".
8. Klicken Sie auf "Bestätigen".
9. Geben Sie im Feld 'Grund' einen Wert ein, oder wählen Sie einen Wert aus.
10. Klicken Sie auf "OK".
11. Klicken Sie im Aktivitätsbereich auf "Allgemein".
12. Klicken Sie auf "Aufträge".
13. Schließen Sie die Seite.


