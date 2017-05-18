---
title: "Überblick über die erweiterte Bankabstimmung"
description: "Mit der erweiterten Bankabstimmungsfunktion können Sie elektronische Bankauszüge importieren und diese in Microsoft Dynamics 365 for Operations mit Bankbuchungen abstimmen.  Dieser Artikel erläutert die Einrichtung von Prozesse für die Abstimmung."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 6c6b171fbba90b02b80c70783ecfd9ab57beb96d
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Überblick über die erweiterte Bankabstimmung

[!include[banner](../includes/banner.md)]


Mit der erweiterten Bankabstimmungsfunktion können Sie elektronische Bankauszüge importieren und diese in Microsoft Dynamics 365 for Operations mit Bankbuchungen abstimmen.  Dieser Artikel erläutert die Einrichtung von Prozesse für die Abstimmung.  

Es gibt mehrere Stück, die vor der Verwendung der erweiterten Bankabstimmungsfunktion eingerichtet werden müssen. Weitere Informationen zur Einrichtung von Bankauszugsimport finden Sie unter [Einrichten von Bankauszugimportprozess](set-up-advanced-bank-reconciliation-import-process.md).  Anforderungen für Einrichtung des Abstimmungsvorgangs sind nachfolgend genauer dargelegt.

## <a name="transaction-codes"></a>Art des Geschäftes
Abstimmungscodes können als Teil von Bankabstimmungsübereinstimmungsregeln verwendet werden.  Transaktionscodes helfen, nur die gleichen Buchungsarten zwischen Dynamics 365 für Operations und Ihrem Bankauszug abzustimmen.  Um diesen Abgleichstyp zu bewerkstelligen, müssen Sie zuerst die Buchungsarten definieren, die für Bankbuchungen von Microsoft Dynamics 365 Operations verwendet werden. Ordnen Sie dann diese Typen den Auszugsbuchungscodes zu, die von der Bank verwendet werden.  Buchungsarten für Dynamics 365 for Operations-Bankbuchungen werden auf der Seite **Bankbuchungsart** definiert.  Dies gilt auch dort, wo Sie das Hauptkonto definieren, das für Buchungen im Zusammenhang mit Transaktionsarten verwendet wird. 

Sobald Ihre Dynamics 365 for Operations-Barnkbuchungscodes definiert werden, ordnen Sie dann diese den Transaktionscodes zu, die in den elektronischen Bankauszügen verwendet werden.  Dieser Zuordnungsprozess wird auf der Seite  **Buchungscode-Zuordnun** ausgeführt.  Die Buchungscode-Zuordnung wird separat für jedes Bankkonto abgeschlossen.

## <a name="matching-rules-and-matching-rule-sets"></a>Zuordnungsregeln und Zuordnungsregelsätze
Übereinstimmungsregeln ermöglichen es Ihnen, Kriterien für automatische Abstimmung zwischen Dynamics 365 for Operations-Bankbuchungen und Bankauszugsbuchungen zu definieren.  Das Einrichten von Übereinstimmungsregeln erfolgt auf der Seite **Abstimmungsübereinstimmungsregeln**.  Weitere Informationen finden Sie unter [Einrichten der Bankabstimmungsabgleichsregel](set-up-bank-reconciliation-matching-rules.md). 

Übereinstimmungsregelnsätze werden verwendet, um eine Gruppe von passenden Regeln zu definieren, die nacheinander während des Bankauszugsabstimmungsprozesses ausgeführt werden.  Übereinstimmungsregelsätze werden auf der Seite  **Abstimmungsübereinstimmungsregelsätz** konfiguriert.

## <a name="cash-and-bank-management-parameters"></a>Bargeld- und Bankverwaltungsparameter
Es gibt einige Parameter, um die erweiterten Bankabstimmungsprozess auf der Seite**Bargeld- und Bankverwaltungsparameter** zu definieren.  **Auszugszeilenbetrag in Soll/Haben anzeigen** ändert die Ansicht des Betrags auf der Seite **Bankauszug**.  Wenn diese Option aktiviert ist, werden die Bankauszugsbuchungsbeträge in separaten Spalten "Soll" und "Haben" angezeigt.  Wenn nicht aktivier, werden Bankauszugsbuchungsbeträge in einer einzelnen Betragsspalte mit dem entsprechenden Vorzeichen angezeigt. 

Die Überprüfungsoptionen, die auf die Parameterseite festgelegt sind, überschreiben die Auswahl, die in den Übereinstimmungsregeln festgelegt sind.  Beispielsweise können Sie Dokumente nicht manuell oder automatisch über die Datumsdifferenz hinaus auf der Parameterseite festlegen.  Falls die Option **Buchungsartzuordnung überprüfen** aktiviert ist, müssen die Buchungsarten zwischen den Dynamics 365 for Operations Bankbuchungen und den Bankauszugsbuchungen zugeordnet werden, um die Buchungen manuell oder automatisch abzugleichen. 

Sie müssen die erforderlichen Nummernkreise für die Seite **Bargeld- und Bankverwaltungsparameter** konfigurieren.  Legen Sie auf der Registerkarte **Nummernkreise** die Nummernkreiscodes für den Download der Referenzen **ID, Auszugs-ID, Abstimmungs-ID und Bankabstimmung** fest.

## <a name="bank-account-reconciliation-options"></a>Optionen für die Bankkontoabstimmung
Sie müssen zuerst die erweitere Bankabstimmung für das Bankkonto aktivieren.  Einige Optionen sind auf der Seite **Bankkonto** verfügbar, sobald die erweiterten Bankabstimmungsfunktionen aktiviert werden. 

Die Funktion **Verwenden von Bankauszüge als Bestätigung für elektronische Zahlung** integriert die Bankabstimmungsfunktion mit dem Status der elektronischen Zahlung.  Wenn dieses aktiviert wird, wird automatisch ein Bankdokument für den elektronischen Zahlungsstatus erstellt und auf **Übermittelt** gesetzt.  Darüber hinaus wird der Status einer elektronischen Zahlung von **Übermittelt** auf **Empfangen** geändert, nachdem die Zahlung zugeordnet, gebucht und abgestimmt ist. 

Das Feld **Bankkontoname im Auszug** ist der Name, der für das Bankkonto auf Ihrem elektronischen Bankauszug verwendet wird.  Dieser Name wird verwendet, wenn bestimmt wird, welche Buchungen für ein Bankkonto aus einem Auszug importiert wird, der Informationen für mehrere Bankkonten enthalten kann. 

Die Option **Nach Import abstimmen** überprüft automatisch den Bankauszug, erstellt eine neue Bankabstimmung und ein Arbeitsblatt und führt den Standardübereinstimmungsregelsatz aus.  Diese Funktionalität automatisiert den Prozess der Abstimmung bis zum Punkt, der manuell abgestimmt werden muss.  Die Einstellungen auf dem Bankkonto wird beim Importieren standardmäßig.




