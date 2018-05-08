---
title: Einrichtung des erweiterten Bankabstimmungsprozesses
description: "Mit der erweiterten Bankabstimmungsfunktion können Sie elektronische Bankauszüge importieren und diese in Microsoft Dynamics 365 for Finance and Operations mit Bankbuchungen abstimmen.  Dieser Artikel erläutert die Einrichtung von Prozesse für die Abstimmung."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: f77a9c927232c95558ba78037f6a6e9f77e202c2
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="advanced-bank-reconciliation-setup-process"></a>Einrichtung des erweiterten Bankabstimmungsprozesses

[!include [banner](../includes/banner.md)]

Mit der erweiterten Bankabstimmungsfunktion können Sie elektronische Bankauszüge importieren und diese in Microsoft Dynamics 365 for Finance and Operations mit Bankbuchungen abstimmen.  Dieser Artikel erläutert die Einrichtung von Prozesse für die Abstimmung.  

Es gibt mehrere Stück, die vor der Verwendung der erweiterten Bankabstimmungsfunktion eingerichtet werden müssen. Weitere Informationen zur Einrichtung von Bankauszugsimport finden Sie unter [Einrichten von Bankauszugimportprozess](set-up-advanced-bank-reconciliation-import-process.md).  Anforderungen für Einrichtung des Abstimmungsvorgangs sind nachfolgend genauer dargelegt.

## <a name="transaction-codes"></a>Art des Geschäftes
Abstimmungscodes können als Teil von Bankabstimmungsübereinstimmungsregeln verwendet werden.  Transaktionscodes helfen, nur die gleichen Buchungsarten zwischen Finance and Operations und Ihrem Bankauszug abzustimmen.  Um diesen Abgleichstyp zu bewerkstelligen, müssen Sie zuerst die Buchungsarten definieren, die für Bankbuchungen von Finance and Operations verwendet werden. Ordnen Sie dann diese Typen den Auszugsbuchungscodes zu, die von der Bank verwendet werden.  Buchungsarten für Finance and Operations-Bankbuchungen werden auf der Seite **Bankbuchungsart** definiert.  Dies gilt auch dort, wo Sie das Hauptkonto definieren, das für Buchungen im Zusammenhang mit Transaktionsarten verwendet wird. 

Sobald Ihre Finance and Operations-Barnkbuchungscodes definiert werden, ordnen Sie dann diese den Transaktionscodes zu, die in den elektronischen Bankauszügen verwendet werden.  Dieser Zuordnungsprozess wird auf der Seite  **Buchungscode-Zuordnun** ausgeführt.  Die Buchungscode-Zuordnung wird separat für jedes Bankkonto abgeschlossen.

## <a name="matching-rules-and-matching-rule-sets"></a>Zuordnungsregeln und Zuordnungsregelsätze
Übereinstimmungsregeln ermöglichen es Ihnen, Kriterien für automatische Abstimmung zwischen Finance and Operations-Bankbuchungen und Bankauszugsbuchungen zu definieren.  Das Einrichten von Übereinstimmungsregeln erfolgt auf der Seite **Abstimmungsübereinstimmungsregeln**.  Weitere Informationen finden Sie unter [Einrichten der Bankabstimmungsabgleichsregel](set-up-bank-reconciliation-matching-rules.md). 

Übereinstimmungsregelnsätze werden verwendet, um eine Gruppe von passenden Regeln zu definieren, die nacheinander während des Bankauszugsabstimmungsprozesses ausgeführt werden.  Übereinstimmungsregelsätze werden auf der Seite  **Abstimmungsübereinstimmungsregelsätz** konfiguriert.

## <a name="cash-and-bank-management-parameters"></a>Bargeld- und Bankverwaltungsparameter
Es gibt einige Parameter, um die erweiterten Bankabstimmungsprozess auf der Seite **Bargeld- und Bankverwaltungsparameter** zu definieren.  **Auszugszeilenbetrag in Soll/Haben anzeigen** ändert die Ansicht des Betrags auf der Seite **Bankauszug**.  Wenn diese Option aktiviert ist, werden die Bankauszugsbuchungsbeträge in separaten Spalten "Soll" und "Haben" angezeigt.  Wenn nicht aktivier, werden Bankauszugsbuchungsbeträge in einer einzelnen Betragsspalte mit dem entsprechenden Vorzeichen angezeigt. 

Die Überprüfungsoptionen, die auf die Parameterseite festgelegt sind, überschreiben die Auswahl, die in den Übereinstimmungsregeln festgelegt sind.  Beispielsweise können Sie Dokumente nicht manuell oder automatisch über die Datumsdifferenz hinaus auf der Parameterseite festlegen.  Falls die Option **Buchungsartzuordnung überprüfen** aktiviert ist, müssen die Buchungsarten zwischen den Finance and Operations Bankbuchungen und den Bankauszugsbuchungen zugeordnet werden, um die Buchungen manuell oder automatisch abzugleichen. 

Sie müssen die erforderlichen Nummernkreise für die Seite **Bargeld- und Bankverwaltungsparameter** konfigurieren.  Legen Sie auf der Registerkarte **Nummernkreise** die Nummernkreiscodes für den Download der Referenzen **ID, Auszugs-ID, Abstimmungs-ID und Bankabstimmung** fest.

## <a name="bank-account-reconciliation-options"></a>Optionen für die Bankkontoabstimmung
Sie müssen zuerst die erweitere Bankabstimmung für das Bankkonto aktivieren.  Einige Optionen sind auf der Seite **Bankkonto** verfügbar, sobald die erweiterten Bankabstimmungsfunktionen aktiviert werden. 

Die Funktion **Verwenden von Bankauszüge als Bestätigung für elektronische Zahlung** integriert die Bankabstimmungsfunktion mit dem Status der elektronischen Zahlung.  Wenn dieses aktiviert wird, wird automatisch ein Bankdokument für den elektronischen Zahlungsstatus erstellt und auf **Übermittelt** gesetzt.  Darüber hinaus wird der Status einer elektronischen Zahlung von **Übermittelt** auf **Empfangen** geändert, nachdem die Zahlung zugeordnet, gebucht und abgestimmt ist. 

Das Feld **Bankkontoname im Auszug** ist der Name, der für das Bankkonto auf Ihrem elektronischen Bankauszug verwendet wird.  Dieser Name wird verwendet, wenn bestimmt wird, welche Buchungen für ein Bankkonto aus einem Auszug importiert wird, der Informationen für mehrere Bankkonten enthalten kann. 

Die Option **Nach Import abstimmen** überprüft automatisch den Bankauszug, erstellt eine neue Bankabstimmung und ein Arbeitsblatt und führt den Standardübereinstimmungsregelsatz aus.  Diese Funktionalität automatisiert den Prozess der Abstimmung bis zum Punkt, der manuell abgestimmt werden muss.  Die Einstellungen auf dem Bankkonto wird beim Importieren standardmäßig.




