---
title: Überprüfung der Bestandsverfügbarkeit
description: Diese Prozedur zeigt Ihnen, wie Sie verfügbaren und physisch verfügbaren Lagerbestand für eine bestimmte Artikelnummer überprüfen.
author: yufeihuang
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c1533dc677c53e90d73077e06a67c71cebc1b7e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574616"
---
# <a name="check-the-availability-of-stock"></a>Überprüfung der Bestandsverfügbarkeit

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt Ihnen, wie Sie verfügbaren und physisch verfügbaren Lagerbestand für eine bestimmte Artikelnummer überprüfen. Darüber hinaus zeigt sie Ihnen, wie Sie Lieferinformationen zu einem Artikel abrufen. Physischer, verfügbarer Lagerbestand ist der verfügbare Lagerbestand, der verfügbar ist – d. h. er ist gekauft, empfangen und erfasst worden. Der verfügbare Lagerbestand umfasst den verfügbaren Lagerbestand, aber auch den Lagerbestand, der bestellt wurde und erwartet wird, aber noch nicht empfangen oder erfasst wurde. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden. Wenn Sie USMF verwenden, können Sie die Beispielswerte verwenden, die angezeigt werden. Diese Aufgaben werden normalerweise von einer Lagerarbeitskraft ausgeführt.


## <a name="check-on-hand-inventory-for-an-item"></a>Verfügbaren Lagerbestand für einen Artikel überprüfen
1. Gehen Sie zu **Navigationsbereich > Module > Lagerverwaltung > Abfragen und Berichte > Verfügbarer Lagerbestand**.
2. Wählen Sie die Zeile **Artikelnummer** aus. Um den verfügbaren Lagerbestand nach Artikelnummer abzufragen, wählen Sie die Zeile aus, in der „Tabelle” auf **Verfügbarer Lagerbestand** und „Feld” auf **Artikelnummer** festgelegt ist.
3. Wählen Sie im Feld **Kriterien** den Artikel aus, den Sie abfragen möchten. Wenn Sie das USMF-Demodatunternehmen verwenden, können Sie "M9201" auswählen.  
4. Klicken Sie auf **OK**.
5. Klicken Sie im **Aktivitätsbereich** auf **Dimensionen**. Die Registerkarte **Dimensionen** ermöglicht es Ihnen, auszuwählen, wie viel Detail Sie über Ihren verfügbaren Lagerbestand sehen möchten. Wenn Sie die Daten benötigen, die der Reservierung zugeordnet sind, müssen Sie alle Lagerbestandsdimensionen für die Artikel anzeigen, die erweiterte Lagerortprozesse verwenden.
6. Klicken Sie auf **OK**.
7. Klicken Sie im **Aktivitätsbereich** auf **Zugehörige Informationen**. Wenn Sie diese Option nicht sehen, müssen Sie möglicherweise auf die Schaltfläche „Auslassungspunkte“ (...) klicken, um zusätzliche Aktivitätsbereichsoptionen anzuzeigen.
8. Klicken Sie auf **Lieferübersicht**. Die Registerkarte **Lieferübersicht** stellt Lieferinformationen für einen bestimmten Artikel bereit, beispielsweise die verfügbare Menge, die Durchlaufzeit und die Kreditordaten.  
9. Erweitern Sie den Abschnitt **Verfügbar**.
10. Erweitern Sie den Abschnitt **Kreditoren**.
11. Schließen Sie die Seite.
12. Schließen Sie die Seite.

## <a name="check-physical-on-hand-inventory"></a>Physischen Lagerbestand überprüfen
1. Gehen Sie zu **Navigationsbereich > Module > Lagerortverwaltung > Abfragen und Berichte > Physischer verfügbarer Bestand**.
2. Geben Sie im Feld **Artikelnummer** einen Wert ein. Sie können die Felder "Standort" und "Lagerort" verwenden, um die Liste der Artikel zu filtern. 
3. Aktualisieren Sie die Seite.
4. Klicken Sie im **Aktivitätsbereich** auf **Dimensionen anzeigen**. Die Registerkarte "Dimensionsanzeige" ermöglicht es Ihnen auszuwählen, wie viel Detail Sie über Ihren verfügbaren Lagerbestand sehen möchten.
5. Klicken Sie auf **OK**.
6. Schließen Sie die Seite.

## <a name="check-on-hand-inventory-by-location"></a>Verfügbaren Lagerbestand nach Lagerplatz überprüfen
1. Gehen Sie zu **Navigationsbereich > Module > Lagerortverwaltung > Abfragen und Berichte > Verfügbar nach Lagerplatz**.
2. Geben Sie im Feld **Lagerort** einen Wert ein. Wenn Sie das USMF-Demodatunternehmen verwenden, können Sie "51 " verwenden.  
3. Aktualisieren Sie die Seite.
4. Klicken Sie auf **Dimensionen anzeigen**.
5. Klicken Sie auf **OK**.
6. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]