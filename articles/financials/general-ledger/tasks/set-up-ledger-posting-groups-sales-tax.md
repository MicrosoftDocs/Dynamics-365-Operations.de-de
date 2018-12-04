--- 
title: "Sachkontobuchungsgruppen für Mehrwertsteuer einrichten"
description: Die Mehrwertsteuer wird zu den Hauptkonten berechnet und gebucht, die in den "Sachkontobuchungsgruppen" angegeben werden.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 15421da6f325dfee22a303e9fe83a0e72895fa08
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Sachkontobuchungsgruppen für Mehrwertsteuer einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Die Mehrwertsteuer wird zu den Hauptkonten berechnet und gebucht, die in den "Sachkontobuchungsgruppen" angegeben werden. Sachkontobuchungsgruppen werden jedem einzelnen Mehrwertsteuercode zugeordnet. Sie können einzelne Sachkontobuchungsgruppen für jeden Mehrwertsteuercode einrichten, eine Sachkontobuchungsgruppe für alle Mehrwertsteuercodes verwenden oder mehrere Sachkontobuchungsgruppen den Mehrwertsteuercodes zuweisen. Für diese Erfassung wird das Demo-Unternehmen DEMF verwendet. 

1. Wechseln Sie zu "Steuer" > "Einstellungen" > "Mehrwertsteuer" > "Sachkontenbuchungsgruppen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Sachkontobuchungsgruppe" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie im Feld "Mehrwertsteuer" das Hauptkonto für ausgehende Mehrwertsteuern aus, die an die Steuerbehörde zu zahlen sind.
    * Mehrwertsteuern werden im Namen der Steuerbehörde erhoben, wenn Sie steuerpflichtige Waren und Dienstleistungen verkaufen.  
6. Wählen Sie im Feld "Vorsteuer" das Hauptkonto für eingehende Steuern aus, die von der Steuerbehörde empfangen werden.
    * Händler erheben Steuern im Auftrag der Steuerbehörde, wenn Sie steuerpflichtige Waren und Dienstleistungen kaufen. Dieses Feld ist nicht verfügbar, wenn die Option "Mehrwertsteuerregeln anwenden" auf der Seite "Hauptbuchparameter" ausgewählt ist. Stattdessen werden an Händler gezahlte Mehrwertsteuerbeträge vom selben Konto abgebucht, wie der Einkauf.   
7. Wählen Sie im Feld "Verbrauchssteuerausgaben" das Hauptkonto für das Buchen abzugsfähiger "Verbrauchssteuern" aus, die nicht eingefordert oder durch Händler der Steuerbehörde gemeldet werden, als Teil der Verlagerung der Steuerschuld GST/HST in der EU.
    * Die Option "Verbrauchssteuer" muss für den "Mehrwertsteuercode" in der Gruppe "Mehrwertsteuer" ausgewählt werden, die in der Transaktion verwendet wird.  Dieses Feld ist nicht verfügbar, wenn die Option "Mehrwertsteuerregeln anwenden" auf der Seite "Hauptbuchparameter" ausgewählt ist.   
8. Wählen Sie im Feld "Gegenkonto Verbrauchssteuer" das Hauptkonto für das Buchen eingehender Verbrauchssteuern aus, die an Steuerbehörden zu zahlen sind.
    * Die Option "Verbrauchssteuer" muss im "Mehrwertsteuercode" in der Gruppe "Mehrwertsteuer" ausgewählt werden, um die "Verbrauchssteuer" zu buchen. Wenn die Option "Mehrwertsteuerregeln anwenden" unter den "Hauptbuchparametern" ausgewählt ist, wird die Gegenbuchung im Ausgabenkonto der Transaktion gebucht.   
9. Wählen Sie im Feld "Ausgleichskonto" das Hauptkonto aus, zu dem der Nettosaldo der Sachkonten gebucht wird, der in den Feldern "Verbrauchssteuer" und "Mehrwertsteuer" angegeben ist.
    * Der Saldo wird erstellt, wenn der "Einzelvorgang für die Abrechnung und Buchung der Mehrwertsteuer" ausgeführt wurde.  Wenn die "Steuerbehörde für den Abrechnungszeitraum" einem Kreditorenkonto zugeordnet ist, wird der Saldo stattdessen zum Kreditorenkonto gebucht.   
10. Wählen Sie im Feld "Kreditorenskonto" das Hauptkonto aus, um Skonto für Mehrwertsteuercodes zu buchen, die dieser "Sachkontobuchungsgruppe" zugeordnet sind.
    * Das ist optional und wenn kein Konto eingegeben wird, wird das Hauptkonto auf Skontobasis verwendet. Es kann hilfreich sein, verschiedene Konten pro Sachkontobuchungsgruppe zu verwenden, wenn Sie die Option zum Stornieren der Mehrwertsteuer auf Skonten bei "Mehrwertsteuergruppen" verwenden.  
11. Wählen Sie im Feld "Debitorenskonto" das Hauptkonto aus, um Skonto für Mehrwertsteuercodes zu buchen, die dieser "Sachkontobuchungsgruppe" zugeordnet sind.
    * Das ist optional und wenn kein Konto eingegeben wird, wird das Hauptkonto für die "Skontocodes" verwendet. Es kann hilfreich sein, verschiedene Konten pro Sachkontobuchungsgruppe zu verwenden, wenn Sie die Option zum Stornieren der Mehrwertsteuer auf Skonten bei "Mehrwertsteuergruppen" verwenden.  
12. Klicken Sie auf "Speichern".


