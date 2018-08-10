--- 
title: Freitextrechnung erstellen
description: Dieser Artikel zeigt, wie eine Freitext-Debitorenrechnung erstellt wird.
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: de-de
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a>Freitextrechnung erstellen

[!include [banner](../includes/banner.md)]

Dieser Artikel zeigt, wie eine Freitext-Debitorenrechnung erstellt wird. Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.

## <a name="create-a-free-text-invoice"></a>Freitextrechnung erstellen

1. Wechseln Sie zu "Debitoren" > "Rechnungen" > "Alle Freitextrechnungen".
2. Klicken Sie auf "Neu".
3. Wählen Sie im Feld "Debitorenkonto" einen Wert aus.
    * Das Rechnungskonto wird standardmäßig auf dasselbe Konto festgelegt, das für das Debitorenkonto verwendet wird.   
    * Der Buchhaltungsstatus beginnt mit "In Bearbeitung", wenn die Rechnung nicht gebucht wird.   
    * Die Rechnungsnummer wird zugewiesen, wenn die Rechnung gebucht wird.  
    * Wenn Sie SEPA-Vollmachten verwenden, wird das Direkteinzugsmandat automatisch mit einer Vollmacht aufgefüllt, wenn Sie das Debitorenkonto auswählen.  
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Geben Sie im Feld "Hauptkonto" eine Kontonummer ohne Dimensionen an.
    * Sie können auch ein oder mehrere Zeichen für das Hauptkonto eingeben und die Suche verwenden, um Ihr Konto zu suchen. Sie geben Dimensionen später in dieser Anleitung ein.  
6. Erweitern Sie das Inforegister "Positionsdetails", sodass Sie Ihrem Hauptkonto Dimensionen hinzufügen können.
7. Klicken Sie auf die Registerkarte "Finanzdimensionsposition".
    * Die Dimensionen sind nur für die ausgewählte Position.    
    * Die Mehrwertsteuergruppe wird vom Debitor aufgefüllt. Wenn der Debitor keine Mehrwertsteuergruppe hat, wird die Mehrwertsteuergruppe aus dem Hauptkonto verwendet.  
    * Die Artikel-Mehrwertsteuergruppe wird vom Hauptkonto aufgefüllt. Wenn das Hauptkonto keine Artikel-Mehrwertsteuergruppe aufweist, wird die Artikel-Mehrwertsteuergruppe in den Mehrwertsteuerparametern für das Hauptbuch verwendet.    
8. Geben Sie im Feld "Menge" eine Zahl ein.
    * Die Menge ist optional.  
9. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.
    * Der Preis je Einheit ist optional.  
    * Der Betrag wird als Menge mal Preis je Einheit berechnet. Sie können diese Berechnung jedoch außer Kraft setzen und einen Betrag eingeben.  
10. Klicken Sie auf "Mehrwertsteuer", um die Mehrwertsteuer anzuzeigen, die für Ihre Rechnung berechnet wird.
    * Zeigen Sie die Mehrwertsteuerbeträge auf dieser Seite an oder Sie können die Beträge auf der Registerkarte "Regulierung" überschreiben.  
11. Klicken Sie auf "OK".
12. Klicken Sie auf "Belastungen", um der Rechnung eine Belastung hinzuzufügen. 
13. Geben Sie im Feld "Belastungen" einen Wert ein.
14. Geben Sie im Feld "Wert der Belastungen" eine Zahl ein.
15. Schließen Sie die Seite.
16. Klicken Sie auf "Summen", um die zusammengefassten Rechnungsdetails und Summen anzuzeigen.
17. Klicken Sie auf "Schließen".
18. Klicken Sie zum Buchen der Rechnung auf "Buchen". Sie können den Vorgang vor dem Buchen abbrechen.
    * So ändern Sie den Zeitpunkt für das Drucken von Rechnungen: Wählen Sie "Aktuell" aus, um jede Rechnung zu drucken, wenn sie aktualisiert wird, oder wählen Sie "Danach" aus, um zu drucken, nachdem alle Rechnungen aktualisiert wurden.  
    * Wenn Sie ändern möchten, wie das Kreditlimit des Debitors vor dem Buchen überprüft wird, ändern Sie den Kreditlimittyp.  
    * Wenn Sie die Rechnung drucken möchten, wählen Sie "Ja" aus.  
    * Wenn Sie die Rechnung buchen möchten, wählen Sie "Ja" aus. Sie können die Rechnung ohne Buchen drucken.  
19. Klicken Sie auf "OK".

## <a name="copy-lines"></a>Positionen kopieren
Um die Positionen auf der Freitextrechnung zu kopieren, wählen Sie eine oder mehrere Positionen aus und gehen anschließend auf ausgewählte Positionen kopieren. Sie können die Anzahl von Kopien angeben, die Sie erstellen möchten, und Sie können Hinweise und Anhänge kopieren. Sie können die Verteilungen kopieren oder zulassen, dass sie neu erstellt werden, wenn Sie buchen. Anschließend können Sie die Informationen nach Bedarf bearbeiten. 

## <a name="create-a-free-text-invoice-from-a-template"></a>Erstellen einer Vorlage für Freitext-Serienrechnungen
Sie können eine Freitext-Rechnung von einer Vorlage erstellen. Wenn Sie Neu von Vorlage aus der Rechnungsregisterkarte auswählen, können Sie einen Vorlagennamen auswählen und der Debitor für die neue Freitextrechnung. Sie können die Standardwerte wie die Zahlungsbedingungen und die Zahlungsmethode der Zahlung auch auswählen oder die Werte verwenden, , die mit der Vorlage gespeichert wurden. Eine neue Freitextrechnung wird erstellt und die Werte in dieser Rechnung bearbeiten. 


