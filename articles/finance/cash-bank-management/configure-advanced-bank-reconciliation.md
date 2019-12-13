---
title: Einrichtung des erweiterten Bankabstimmungsprozesses
description: Mit der erweiterten Bankabstimmungsfunktion können Sie elektronische Bankauszüge importieren und diese in Microsoft Dynamics 365 Finance automatisch mit Bankbuchungen abstimmen. Dieser Artikel erläutert die Einrichtung von Prozessen für die Abstimmung.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 405af4e3e122953bbfa74e7e91d2feef8f068708
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772627"
---
# <a name="advanced-bank-reconciliation-setup-process"></a>Einrichtung des erweiterten Bankabstimmungsprozesses

[!include [banner](../includes/banner.md)]

Mit der erweiterten Bankabstimmungsfunktion können Sie elektronische Bankauszüge importieren und diese in Microsoft Dynamics 365 Finance automatisch mit Bankbuchungen abstimmen. Dieser Artikel erläutert die Einrichtung von Prozesse für die Abstimmung.  

Es gibt mehrere Stück, die vor der Verwendung der erweiterten Bankabstimmungsfunktion eingerichtet werden müssen. Weitere Informationen zur Einrichtung von Bankauszugsimport finden Sie unter [Einrichten des erweiterten Bankabstimmungs-Importprozesses](set-up-advanced-bank-reconciliation-import-process.md).  Anforderungen für Einrichtung des Abstimmungsvorgangs sind nachfolgend genauer dargelegt.

## <a name="transaction-codes"></a>Art des Geschäftes
Abstimmungscodes können als Teil von Bankabstimmungsübereinstimmungsregeln verwendet werden. Transaktionscodes helfen, nur die gleichen Buchungsarten zwischen Finance und Ihrem Bankauszug abzustimmen. Um diesen Abgleichstyp zu bewerkstelligen, müssen Sie zuerst die Transaktionsarten definieren, die für Banktransaktionen von Finance verwendet werden. Ordnen Sie dann diese Typen den Auszugstransaktionscodes zu, die von der Bank verwendet werden. Transaktionsarten für Banktransaktionen werden auf der Seite **Banktransaktionsart** definiert. Dies gilt auch dort, wo Sie das Hauptkonto definieren, das für Buchungen im Zusammenhang mit Transaktionsarten verwendet wird. 

Sobald Ihre Banktransaktionscodes definiert werden, ordnen Sie dann diese den Transaktionscodes zu, die in den elektronischen Bankauszügen verwendet werden. Dieser Zuordnungsprozess wird auf der Seite  **Buchungscode-Zuordnun** ausgeführt. Die Buchungscode-Zuordnung wird separat für jedes Bankkonto abgeschlossen.

## <a name="matching-rules-and-matching-rule-sets"></a>Zuordnungsregeln und Zuordnungsregelsätze
Übereinstimmungsregeln ermöglichen es Ihnen, Kriterien für automatische Abstimmung zwischen Finance-Banktransaktionen und Bankauszugstransaktionen zu definieren. Das Einrichten von Übereinstimmungsregeln erfolgt auf der Seite **Abstimmungsübereinstimmungsregeln**. Weitere Informationen finden Sie unter [Einrichten der Bankabstimmungsabgleichsregel](set-up-bank-reconciliation-matching-rules.md). 

Übereinstimmungsregelnsätze werden verwendet, um eine Gruppe von passenden Regeln zu definieren, die nacheinander während des Bankauszugsabstimmungsprozesses ausgeführt werden.  Übereinstimmungsregelsätze werden auf der Seite  **Abstimmungsübereinstimmungsregelsätz** konfiguriert.

## <a name="cash-and-bank-management-parameters"></a>Bargeld- und Bankverwaltungsparameter
Es gibt einige Parameter, um die erweiterten Bankabstimmungsprozess auf der Seite **Bargeld- und Bankverwaltungsparameter** zu definieren.  **Auszugszeilenbetrag in Soll/Haben anzeigen** ändert die Ansicht des Betrags auf der Seite **Bankauszug**. Wenn diese Option aktiviert ist, werden die Bankauszugsbuchungsbeträge in separaten Spalten "Soll" und "Haben" angezeigt. Wenn nicht aktivier, werden Bankauszugsbuchungsbeträge in einer einzelnen Betragsspalte mit dem entsprechenden Vorzeichen angezeigt. 

Die Überprüfungsoptionen, die auf die Parameterseite festgelegt sind, überschreiben die Auswahl, die in den Übereinstimmungsregeln festgelegt sind. Beispielsweise können Sie Dokumente nicht manuell oder automatisch über die Datumsdifferenz hinaus auf der Parameterseite festlegen. Falls die Option **Transaktionsartzuordnung überprüfen** aktiviert ist, müssen die Transaktionsarten zwischen den Finance-Banktransaktionen und den Bankauszugstransaktionen zugeordnet werden, um die Buchungen manuell oder automatisch abzugleichen. 

Sie müssen die erforderlichen Nummernkreise für die Seite **Bargeld- und Bankverwaltungsparameter** konfigurieren.  Legen Sie auf der Registerkarte **Nummernkreise** die Nummernkreiscodes für den Download der Referenzen **ID, Auszugs-ID, Abstimmungs-ID und Bankabstimmung** fest.

## <a name="bank-account-reconciliation-options"></a>Optionen für die Bankkontoabstimmung
Sie müssen zuerst die erweitere Bankabstimmung für das Bankkonto aktivieren. Einige Optionen sind auf der Seite **Bankkonto** verfügbar, sobald die erweiterten Bankabstimmungsfunktionen aktiviert werden. 

Die Funktion **Verwenden von Bankauszüge als Bestätigung für elektronische Zahlung** integriert die Bankabstimmungsfunktion mit dem Status der elektronischen Zahlung. Wenn dieses aktiviert wird, wird automatisch ein Bankdokument für den elektronischen Zahlungsstatus erstellt und auf **Übermittelt** gesetzt. Darüber hinaus wird der Status einer elektronischen Zahlung von **Übermittelt** auf **Empfangen** geändert, nachdem die Zahlung zugeordnet, gebucht und abgestimmt ist. 

Das Feld **Bankkontoname im Auszug** ist der Name, der für das Bankkonto auf Ihrem elektronischen Bankauszug verwendet wird. Dieser Name wird verwendet, wenn bestimmt wird, welche Buchungen für ein Bankkonto aus einem Auszug importiert wird, der Informationen für mehrere Bankkonten enthalten kann. 

Die Option **Nach Import abstimmen** überprüft automatisch den Bankauszug, erstellt eine neue Bankabstimmung und ein Arbeitsblatt und führt den Standardübereinstimmungsregelsatz aus. Diese Funktionalität automatisiert den Prozess der Abstimmung bis zum Punkt, der manuell abgestimmt werden muss. Die Einstellungen auf dem Bankkonto wird beim Importieren standardmäßig.



