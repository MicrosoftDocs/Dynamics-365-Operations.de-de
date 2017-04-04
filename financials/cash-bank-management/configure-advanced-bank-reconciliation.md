---
title: "Überblick über die erweiterte Bankabstimmung"
description: "Erweiterte Bankabstimmung es Ihnen ermöglicht, zu importieren und elektronische Bankauszüge mit Bankbuchungen in Microsoft Dynamics 365 für Arbeitsgänge automatisch auszugleichen.  Dieser Artikel erläutert die Einrichtung von Prozesse für die Abstimmung."
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
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: c2fc9e858f61d7d0122393bbf306ba64ac3659b8
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Überblick über die erweiterte Bankabstimmung

Erweiterte Bankabstimmung es Ihnen ermöglicht, zu importieren und elektronische Bankauszüge mit Bankbuchungen in Microsoft Dynamics 365 für Arbeitsgänge automatisch auszugleichen.  Dieser Artikel erläutert die Einrichtung von Prozesse für die Abstimmung.  

Es gibt mehrere Stück, die vor der Verwendung der Bankabstimmungsfunktionen erweiterten eingerichtet werden müssen. Weitere Informationen zu Aufstellungsbankauszugsimport, finden Sie unter den Bankauszugsimportprozess [] (setup-advanced-bank-reconciliation-import-process.md) einrichten.  Anforderungen für Einrichtung des Abstimmungsvorgangs Folgenden sind genauer.

## <a name="transaction-codes"></a>Art des Geschäftes
Art des Geschäftes können als Teil von Bankabstimmungsübereinstimmungsregeln verwendet werden.  Art des Geschäftes unterstützen, nur die gleichen Buchungsarten zwischen Dynamics 365 für Arbeitsgänge und den Bankauszug abstimmen.  Um diesen Abgleichstyp zu bewerkstelligen, müssen Sie zuerst die Buchungsarten definieren, die für Bankbuchungen von Microsoft Dynamics 365 für Arbeitsgänge verwendet werden, und ordnen diesen Typen zu den Auszugsarten des geschäfts, auf die von der Bank verwendet werden.  Buchungsarten für Dynamics 365 für Arbeitsgangsbankbuchungen werden auf der Seite ** Bankbuchungsart ** definiert.  Dies gilt auch, wo Sie definieren das für die Buchungen verwendet werden Hauptkonto, die mit der Buchungsart zusammenhängen. 

Sobald das Dynamics 365 für Arbeitsgangsbankbuchungscodes definiert werden, ordnen Sie dann die zu den Arten des Geschäftes für, die in den elektronischen Bankauszügen verwendet werden.  Dieser ist mithilfe der Zuordnungsprozess ** Art des Geschäftsen-Zuordnung ** Seite ausgeführt.  Art des Geschäftsen-Zuordnung wird separat für jedes Bankkonto manuell abgeschlossen.

## <a name="matching-rules-and-matching-rule-sets"></a>Zuordnungsregeln und Zuordnungsregelsätze
Übereinstimmungsregeln ermöglichen, um Kriterien für automatische Abstimmung zwischen Dynamics 365 für Arbeitsgangsbankbuchungen und Bankauszugsbuchungen zu definieren.  Einrichten von Übereinstimmungsregeln ist an Abstimmungsübereinstimmungsregeln erfolgte ** ** Seite.  Weitere Informationen finden Sie Bankabstimmungsübereinstimmungsregeln []( setup-bank-reconciliation-matching-rules.md) einrichten. 

Übereinstimmungsregelsätze werden verwendet, um eine Gruppe Übereinstimmungsregeln zu definieren, die während des Bankabstimmungsprozesses nacheinander ausgeführt werden.  Übereinstimmungsregelsätze werden auf der Seite Abstimmungsübereinstimmungsregelsätze ** ** konfiguriert.

## <a name="cash-and-bank-management-parameters"></a>Bargeld- und Bankverwaltungsparameter
Es gibt einige Parameter, um die erweiterten Bankabstimmungsprozess auf der Landes- oder ** Bargeld- und Bankverwaltungsparameter ** Seite.  ** Die im Showaufstellungszeilebetrag Soll/in Soll- ** Änderungen die Ansicht von Beträgen auf der Bankauszug ** ** Seite.  Wenn diese Option aktiviert ist, werden die Bankauszugsbuchungsbeträge in anderen Spalten "Soll" und "Haben" angezeigt.  Wenn sie nicht ausgewählt, werden Bankauszugsbuchungsbeträge einzelnen in einer Betragsspalte mit dem entsprechenden Vorzeichen angezeigt. 

Folgende Überprüfungsoptionen, die auf die Parameterseite festgelegt sind, setzen die Auswahl, die im Übereinstimmungsregeln festgelegt wird.  Beispielsweise können Sie Dokumente zu der Datumsdifferenz hinaus nicht manuell oder automatisch auf die Parameterseite übereinstimmen festgelegt.  Falls die Option ** überprüfen Sie Buchungsartzuordnung ** aktiviert ist, müssen die Buchungsarten zwischen den Dynamics 365 Bankbuchung für Arbeitsgänge und Bankauszugsbuchung, damit die Buchungen zugeordnet werden manuell oder automatisch abgeglichen. 

Sie müssen die erforderlichen Nummernkreise für die Bargeld- und Bankverwaltungsparameter ** ** Seite auch mit dem konfigurieren.  Wählen Sie auf der Registerkarte Nummernkreise ** ** Legen Sie Nummernkreiscodes für den Download ** Kennung, Auszug Kennung, ob Sie Kennung und Bankabstimmung ab ** Referenzen fest.

## <a name="bank-account-reconciliation-options"></a>Optionen für die Bankkontoabstimmung
Sie müssen für erweiterte Bankabstimmung das Bankkonto zunächst aktivieren.  Einige Optionen sind auf der verfügbar ** Bankkonto ** Seite, sobald die erweiterten Bankabstimmungsfunktionen aktiviert werden. 

** Verwenden Sie als Bankauszüge Bestätigung elektronischer Zahlung ** Funktionen die Integration Bankabstimmungsfunktionen mit Status der elektronischen Zahlung.  Wenn dieses aktiviert wird, wird automatisch für ein Bankdokument den Status der elektronischen Zahlung ist festgelegt auf erstellt ** ** übermittelt.  Darüber hinaus wird der Status einer elektronischen Zahlung aus aktualisiert ** übermittelt ** ** zu empfangen ** nachdem die Zahlung zugeordnet ist, gebucht und abgestimmt. 

Das Bankkontoname ** in Auszügen ** Feld ist der Name, der für das Bankkonto in den elektronischen Bankauszügen verwendet wird.  Dieser Name wird verwendet, wenn von bestimmt, welche für ein Bankkonto aus einem Kontoauszug zu importieren, Buchungen, der möglicherweise Informationen für mehrere Bankkonten enthält. 

Die Option ** Stimmen Sie nach dem Import aus ** überprüft automatisch den Bankauszug, stellt eine neue Bankabstimmung und ein Arbeitsblatt erstellen und führt den Standardübereinstimmungsregelsatz aus.  Diese Funktionen automatisieren den Prozess bis so weit der Buchungen, die manuell in Übereinstimmung gebracht werden müssen.  Die Einstellungen auf dem Bankkonto wird standardmäßig beim Importieren.


