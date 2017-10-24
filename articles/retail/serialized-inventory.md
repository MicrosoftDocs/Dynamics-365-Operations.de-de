---
title: "POS-Verbesserungen für serialisierte Produkte"
description: "In diesem Thema werden Verbesserungen aufgelistet, die an serialisierten Produkten vorgenommen wurden, damit Sie Zeit sparen können und produktiver sind."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 214452d0f40265c0ed9fac7a74844ad89782257d
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="pos-improvements-for-serialized-products"></a>POS-Verbesserungen für serialisierte Produkte

[!include[banner](includes/banner.md)]

## <a name="overview"></a>Überblick 
Basierend auf den Einstellungen in „Retail Zentralverwaltung” können Produkte entweder als serialisiert oder als nicht serialisiert klassifiziert werden. Wenn Produkte serialisiert sind, kann jedem Artikel eine eindeutige Nummer zugewiesen werden. Das erleichtert die Nachverfolgung von Garantien, von Artikeln sowie die Bestätigung des Besitzes. Obwohl die Möglichkeit der Angabe von Seriennummern für serialisierte Produkte in unserer Modern/Cloud Point of Sale (POS) vorhanden war, sind einige Verbesserungen hinzugefügt worden. So können Kassierer Zeit sparen und produktiver sein.  

## <a name="pos-improvements"></a>POS-Verbesserungen

- **Seriennummern sind erst beim Auschecken erforderlich** – Zuvor musste ein Kassierer, der einer Transaktion ein serialisiertes Produkt hinzufügte eine Seriennummer angeben. Diese Anforderung wurde ein Problem in Kundenkontaktszenarien, wenn Kassierer und Vertriebsmitarbeiter eine Chance hatten, zusätzliche Produkte zu verkaufen. Bis zum Zahlungsschritt wurden die Produkte oft im Warenkorb aktualisiert. Daher forderte jedes Mal, wenn ein Kassierer/eine Kassiererin ein neues Produkt hinzufügte, das System ihn oder sie dazu auf, die Seriennummer einzugeben. Das Seriennummerndialogfeld enthält jetzt eine Schaltfläche **Später hinzufügen**. Daher können die Vertriebsmitarbeiter den Artikel der Transaktion hinzufügen, aber die Seriennummer später angeben. Vertriebsmitarbeiter können serialisierte Artikel in einem Warenkorb schnell hinzufügen und ersetzen und dann die Seriennummer erst kurz vor dem Auschecken angeben. Wenn die Seriennummer für irgendein serialisiertes Produkt nicht angegeben wird, erhält ein Kassierer, der versucht, die Transaktion abzuschließen, eine Fehlermeldung. Diese Nachricht gibt an, dass der Kassierer/die Kassiererin die fehlenden Seriennummern angeben muss, bevor er/sie fortfahren kann.

    Für jeden serialisierten Artikel, bei dem die Seriennummer übersprungen wurde, erscheint ein Kommentar unter der Transaktionsposition. Dieser Kommentar gibt an, dass die Seriennummer für den Artikel nicht angegeben wurde. Daher kann der Kassierer schnell Artikel finden, bei denen eine Seriennummer fehlt.

    Ein neuer Arbeitsgang **Seriennummer hinzufügen** stellt auch die Seriennummer für Artikel bereit, denen eine Seriennummer fehlt. Nachdem die Seriennummer angegeben wurde, kann sie nicht bearbeitet werden. Der Kassierer muss die Position stornieren und das Produkt erneut hinzufügen. 
    
- **Seriennummern sind nicht erforderlich, um Debitorenaufträge erteilen zu können** – Debitorenaufträge können in einem Shop erteilt werden und in einem anderen ausgeführt werden. Ein Kassierer, der einen Kundenauftrag erteilt, muss nicht die Seriennummer angeben. Die Seriennummer wird während der Entnahme oder des Entnahmeschritts angegeben. Eine Seriennummer muss jedoch für alle Positionsartikel angegeben werden, für die der Liefertyp **Zum Mitnehmen** ausgewählt ist. Andernfalls kann die Transaktion nicht abgeschlossen werden.    
- **Serialisierte Produkte werden nicht in der Buchungsansicht aggregiert** – Die Einstellung **Produkte aggregieren** in der Feldgruppe **Terminal** auf der Seite **Funktionsprofil** ermöglicht es ihnen, dieselben nicht serialisierten Produkte in der Buchungsansicht zu aggregieren. Wenn dieselben Produkte aggregiert werden, können sie leichter im Transaktionsraster angezeigt werden. Da jedoch Seriennummern im Allgemeinen eindeutig sind und Vertriebsmitarbeiter keine Seriennummern bis zum Auschecken eingeben müssen, gilt die Einstellung **Produkte aggregieren** nicht für serialisierte Produkte. Daher werden serialisierte Produkte nicht in der Transaktionsansicht aggregiert, wenn die Einstellung **Produkte aggregieren** aktiviert ist.

