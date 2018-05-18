---
title: Sperrung von Lagerbestand erstellen und verwalten
description: "Im folgenden Verfahren wird dargestellt, wie verhindert wird, dass physisch verfügbarer Lagerbestand durch andere ausgehende Quelldokumente mithilfe der Sperrung von Lagerbestand reserviert wird."
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7272349cf16b9459823a752b8d3df915f42606ef
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-maintain-inventory-blocking"></a>Sperrung von Lagerbestand erstellen und verwalten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Im folgenden Verfahren wird dargestellt, wie verhindert wird, dass physisch verfügbarer Lagerbestand durch andere ausgehende Quelldokumente mithilfe der Sperrung von Lagerbestand reserviert wird. Sie können die Prozedur im Demodatenunternehmen USMF mit den Beispielswerten ausführen, die angezeigt werden. Sie müssen einen Artikel mit physisch verfügbarem Lagerbestand haben, bevor Sie dieses Verfahren beginnen.


## <a name="create-an-inventory-blocking"></a>Erstellen einer Sperrung von Lagerbestand
1. Wechseln Sie zu "Lagerverwaltung" > "Periodische Aufgaben" > "Sperrung von Lagerbestand".
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Wählen Sie in der Liste den Artikel aus.
    * Wählen Sie eine Artikelnummer mit physischem Lagerbestand aus, die Sie sperren möchten. Wenn Sie USMF verwenden, können Sie Artikel M9201 auswählen.  
5. Geben Sie im Feld "Menge" eine Zahl ein.
    * Wenn Sie Artikel M9201 verwenden, müssen Sie weniger als 200 auswählen.  
6. Schalten Sie die Erweiterung des Abschnitts "Lagerungsdimensionen" ein/aus.
7. Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wenn Sie Artikel M9201 verwenden, können Sie Warehouse 51 auswählen.  
9. Klicken Sie auf "Speichern".

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Aktualisieren Sie die Bedingungen der Sperrung von Lagerbestand
1. Geben Sie im Feld "Menge" eine Zahl ein.
    * Aktualisieren Sie das Felde "Lagermenge", um die zu sperrende Menge wiederzugeben.  
2. Geben Sie im Feld "Erwartetes Datum" ein Datum ein.
    * Sie sollten angeben, wann damit gerechnet wird, dass der gesperrte Bestand für die Reservierung verfügbar wird, indem Sie ein erwartetes Datum zuweisen. Wenn die Option "Erwartete Zugänge" für die Sperrung des Lagerbestands aktiviert ist (Standardeinstellung, wenn Sie manuell eine Sperrung erstellen), wird dieses Datum auf der erwarteten Buchung angezeigt.  
3. Klicken Sie auf "Speichern".

## <a name="remove-the-inventory-blocking"></a>Sperrung von Lagerbestand entfernen
1. Klicken Sie auf Löschen.
2. Klicken Sie auf "Ja".
3. Schließen Sie die Seite.

