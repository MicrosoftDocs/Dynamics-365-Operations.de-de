--- 
title: "Überprüfung der Bestandsverfügbarkeit"
description: "Diese Prozedur zeigt Ihnen, wie Sie verfügbaren und physisch verfügbaren Lagerbestand für eine bestimmte Artikelnummer überprüfen."
author: 
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: 
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: 
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62338fe11c30781f264e626fad835a2ba9dca837
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="check-the-availability-of-stock"></a>Überprüfung der Bestandsverfügbarkeit

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen, wie Sie verfügbaren und physisch verfügbaren Lagerbestand für eine bestimmte Artikelnummer überprüfen. Darüber hinaus zeigt sie Ihnen, wie Sie Lieferinformationen zu einem Artikel abrufen. Physischer, verfügbare Lagerbestand ist der verfügbare Lagerbestand, der verfügbar ist – d. h. er ist gekauft, empfangen und erfasst worden. Der verfügbare Lagerbestand umfasst den verfügbaren Lagerbestand, aber auch den Lagerbestand, der bestellt wurde und erwartet wird, der aber noch nicht empfangen oder erfasst wurde. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden. Wenn Sie USMF verwenden, können Sie die Beispielswerte verwenden, die angezeigt werden. Diese Aufgaben werden normalerweise von einer Lagerarbeitskraft ausgeführt.


## <a name="check-on-hand-inventory-for-an-item"></a>Verfügbaren Lagerbestand für einen Artikel überprüfen
1. Wechseln Sie zu "Lagerverwaltung" > "Abfragen und Berichte" > "Verfügbarer Lagerbestand".
2. Wählen Sie die "Artikelnummerzeile" aus.
    * Um den verfügbaren Lagerbestand nach Artikelnummer abzufragen, wählen Sie die Zeile aus, in der die "Tabelle" auf "Verfügbarer Lagerbestand" und "Feld" auf "Artikelnummer" festgelegt ist.  
3. Wählen Sie im Feld "Kriterien" den Artikel aus, den Sie abfragen möchten.
    * Wenn Sie das USMF-Demodatunternehmen verwenden, können Sie "M9201" auswählen.  
4. Klicken Sie auf "OK".
5. Klicken Sie auf "Dimensionen".
    * Die Registerkarte "Dimensionen" ermöglicht es Ihnen auszuwählen, wie viel Detail Sie über Ihren verfügbaren Lagerbestand sehen möchten. Wenn Sie die Daten benötigen, die der Reservierung zugeordnet sind, müssen Sie alle Lagerbestandsdimensionen für die Artikel anzeigen, die erweiterte Lagerortprozesse verwenden.  
6. Klicken Sie auf "OK".
7. Klicken Sie im Aktivitätsbereich auf "Zugehörige Informationen".
    * Wenn Sie das nicht sehen, müssen Sie möglicherweise auf der Schaltfläche "Auslassungspunkte" (...) klicken, um zusätzliche Aktionsbereichsoptionen anzuzeigen.  
8. Klicken Sie auf "Lieferübersicht".
    * Die Registerkarte "Lieferübersicht" stellt Lieferinformationen für einen bestimmten Artikel bereit, beispielsweise die verfügbare Menge, die Durchlaufzeit und die Kreditordaten.  
9. Erweitern Sie den Abschnitt "Verfügbar".
10. Erweitern Sie den Abschnitt "Kreditoren".
11. Schließen Sie die Seite.
12. Schließen Sie die Seite.

## <a name="check-physical-on-hand-inventory"></a>Physischen Lagerbestand überprüfen
1. Wechseln Sie zu "Lagerortverwaltung" > "Abfragen und Berichte" > "Physischer Lagerbestand".
2. Geben Sie im Feld "Artikelnummer" einen Wert ein.
    * Sie können die Felder "Standort" und "Lagerort" verwenden, um die Liste der Artikel zu filtern.  
3. Aktualisieren Sie die Seite.
4. Klicken Sie auf "Dimensionen anzeigen".
    * Die Registerkarte "Dimensionsanzeige" ermöglicht es Ihnen auszuwählen, wie viel Detail Sie über Ihren verfügbaren Lagerbestand sehen möchten.  
5. Klicken Sie auf "OK".
6. Schließen Sie die Seite.

## <a name="check-on-hand-inventory-by-location"></a>Verfügbaren Lagerbestand nach Lagerplatz überprüfen
1. Wechseln Sie zu "Lagerortverwaltung" > "Abfragen und Berichte" > "Verfügbar nach Lagerplatz".
2. Geben Sie im Feld "Lagerort" einen Wert ein.
    * Wenn Sie das USMF-Demodatunternehmen verwenden, können Sie "51 " verwenden.  
3. Aktualisieren Sie die Seite.
4. Klicken Sie auf "Dimensionen anzeigen".
5. Klicken Sie auf "OK".
6. Schließen Sie die Seite.


