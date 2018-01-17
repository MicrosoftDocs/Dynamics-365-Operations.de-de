---
title: Produktlebenszyklus-Status
description: Ein Produktlebenszyklusstatus dokumentiert den Lebenszyklusstatus eines freigegebenen Produkts oder Produktvariante.
author: cvocph
manager: AnnBe
ms.date: 12/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core (Operations, Core)
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: cvocph
ms.dyn365.ops.intro: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: 33130a4061f22335aeeffa69c478b693604393a9
ms.openlocfilehash: a57f306ba02c5758c39c4bd29d9a4fa0d7efbcd3
ms.contentlocale: de-de
ms.lasthandoff: 12/20/2017

---

# <a name="product-lifecycle-state"></a>Produktlebenszyklus-Status 

[!include[banner](../includes/banner.md)]


Ein Produktlebenszyklusstatus dokumentiert den Lebenszyklusstatus eines freigegebenen Produkts oder Produktvariante. Produktlebenszyklusstatus werden vom Benutzer, in der Regel ein Produktmanager oder ein Produktmasterdatenmanager, definiert. Bestimmte Geschäftsprozesse, wie Produktprogrammplan, können von einem bestimmten Lebenszyklusstatus betroffen sein.   
 
Ein freigegebenes Produkt oder Produktvariante können einem Produktlebenszyklusstatus zugeordnet werden, der dokumentiert, in welchem Lebenszyklusstatus sich ein bestimmtes Produkt oder eine bestimmte Variante gerade befindet. Sie können eine beliebige Anzahl von Produktlebenszyklusstatus definieren, indem Sie einen Statusname und eine Beschreibung zuweisen. Sie können einen Lebenszyklusstatus als Standardstatus für neu freigegebene Produkte auswählen. Freigegebene Produktvarianten erben ihren Produktlebenszyklusstatus von ihrem freigegebenen Produktmaster bei der Erstellung. Wenn Sie den Lebenszyklusstatus bei einem freigegebenen Produktmaster ändern, können Sie wählen, dass alle vorhandenen Varianten aktualisiert werden, die denselben ursprünglichen Status haben.  

## <a name="create-a-new-product-lifecycle-state"></a>Erstellen eines neuen Produktlebenszyklusstatus 
 
- Um einen neuen Produktlebenszyklusstatus zu erstellen, geben Sie den Aufgabenleitfaden wieder oder lesen Sie ihn: **Einen neuen Produktlebenszyklusstatus erstellen**. 

-  Um einen standardmäßigen Produktlebenszyklusstatus zu erstellen, geben Sie den Aufgabenleitfaden wieder oder lesen Sie ihn: **Einen neuen standardmäßigen Produktlebenszyklusstatus erstellen**.   

## <a name="associate-product-lifecycle-states-to-released-products"></a>Produktlebensyklusstatus freigegebenen Produkten zuordnen  

Es gibt mehrere Möglichkeiten, einen Produktlebenszyklusstatus freigegebenen Produkten oder Produktvarianten zuzuordnen.

-  Bei Erstellung eines neuen freigegebenen Produkts wird der standardmäßige **Produktlebenszyklusstatus** automatisch zugewiesen. 
-  Bei Freigabe eines Produkts für eine juristische Person wird der standardmäßige **Produktlebenszyklusstatus** automatisch zugewiesen. 
-  Bei Freigabe einer Produktvariante für eine juristische Person wird der **Produktlebenszyklusstatus**, der dem freigegebenen Produktmaster in dieser juristischen Person zugeordnet ist, automatisch der neuen Variante zugewiesen. 

Sie können den Produktlebenszyklusstatus manuell aktualisieren mithilfe von: 

-    Die Listenseite **Freigegebene Produkte** oder **Detailansicht**. 
-  Die Listenseite **Freigegebene Produktvarianten** oder **Detailansicht**. 
-  Suchen Sie die veralteten Produkte oder Produktvarianten auf Grundlage von Bedarf und ordnen Sie einen Lebenszyklusstatus zu.  

Um ausführliche Informationen dazu zu erhalten, wie Produktlebenszyklusstatus zugeordnet werden, geben Sie die folgenden Aufgabenleitfäden wieder oder lesen Sie diese.

-  Um einen Produktlebenszyklusstatus einem freigegebenen Produktmaster zuzuordnen, geben Sie den folgenden Aufgabenleitfaden wieder oder lesen Sie ihn: **Ein Produktlebenszyklusstatus einem freigegebenen Produktmaster zuweisen**. 

-  Um einen Produktlebenszyklusstatus einem Freigabeprodukt zuzuordnen, geben Sie den folgenden Aufgabenleitfaden wieder oder lesen Sie ihn: **Ein Produktlebenszyklusstatus einem freigegebenen Produktmaster zuweisen**. 

## <a name="impact-on-master-planning"></a>Auswirkung auf Produktprogrammplan 

Der Produktlebenszyklusstatus hat nur ein Steuerungskennzeichen: **Ist aktiv für die Planung**. Standardmäßig ist dieses auf **Ja** für alle erstellten Produktlebenszyklusstatus festgelegt, doch es kann zu **Nein** geändert werden. Wenn es auf **Nein** festgelegt ist, sind die zugeordneten freigegebenen Produkte oder freigegebenen Produktvarianten Folgende: 

-  Ausgeschlossen aus dem Produktprogrammplan. 
-  Ausgeschlossen aus der Stücklistenebeneberechnung. 

Um ausführliche Informationen dazu zu erhalten, wie mithilfe eines Produktlebenszyklusstatus Produkte von der Produktprogrammplanung und der Stücklistenebenenberechnung ausgeschlossen werden können, geben Sie den Aufgabenleitfaden **Erstellen eines Produktlebenszyklusstatus, um Produkte vom Produktprogrammplan auszuschließen** wieder oder lesen Sie ihn.

> [!NOTE]
> Aus Leistungsgründen wird dringend empfohlen, alle veralteten freigegebenen Produkte oder Produktvarianten zuzuordnen, insbesondere wenn Sie mit nicht wiederverwendbaren Produktkonfigurationsvarianten arbeiten, mit einem Produktlebensyklusstatus, der für den Produktprogrammplan deaktiviert ist.  
 
## <a name="default-migration-import-and-export"></a>Standardmäßige Migration, Import und Export 

Die Produktlebenszyklusstatus werden durch Datenentitäten nicht unterstützt, und der Lebenszyklusstatus kann nicht auf einen variables Status durch die freigegebenen Produktdatenentitäten festgelegt werden.

-  Nach der Migration von vorherigen Versionen, ist der Lebenszyklusstatus aller Produkte und Produktvarianten leer.  
-  Wenn die freigegebenen Produkte durch eine Datenentität importiert werden, wird bei der Erstellung der Standardlebenszyklusstatus angewendet.  
-  Wenn Sie freigegebene Produktvarianten durch eine Datenentität importieren, wird der Produktlebenszyklusstatus des freigegebenen Produktmasters importiert.   
 
## <a name="find-obsolete-products-and-products-variants"></a>Veraltete Produkte und Produktvarianten suchen 
 
Sie können eine Simulationsanalyse ausführen, um veraltete freigegebene Produkte oder Produktvarianten zu finden, und dann ihren Produktlebenszyklusstatus aktualisieren. Um veraltete Produkte zu finden, geben Sie den Aufgabenleitfaden **Veraltete Produktvarianten suchen und einen Produktlebenszyklusstatus zuweisen** wieder und lesen Sie ihn. Dieser Aufgabenleitfaden zeigt, wie Sie veraltete freigegebene Produkte oder Produktvarianten finden und wie Sie den veralteten Produkten einen Produktlebenszyklusstatus zuordnen. Er zeigt auch, wie Simulationsergebnisse angezeigt werden und wie beurteilt wird, wie viele Produkte und Produktvarianten einem neuen Produktlebenszyklusstatus zugeordnet werden, wenn das Update ohne Simulation ausgeführt wird.  
 
Indem Sie die Analyse in einem Simulationsmodus ausführen, werden die Produkte und Produktvarianten, die als veraltet identifiziert werden, in einem spezifischen Formular angezeigt, in dem sie einfach überprüft werden können. Durch die Analyse wird nach Transaktionen und spezifischen Masterdaten gesucht, um Produkte zu identifizieren, für die es keinen Bedarf innerhalb einer variablen Periode gibt und keine Masterdaten, die in einem Bedarf resultieren können. Neue freigegebene Produkte innerhalb einer variablen Periode können aus der Analyse ausgeschlossen werden. Wenn die Analysesimulation das erwartete Ergebnis zurückgibt, kann der Benutzer die Analyse ausführen und einen neuen Produktlebenszyklusstatus für alle Produkte festlegen, die durch die Analyse als veraltet identifiziert wurden.  
 
> [!NOTE]
> Beachten Sie, dass sämtliche Analysen und Updates innerhalb derselben juristischen Person erfolgen müssen.  
 
## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Kriterien zum Auswählen und Aktualisieren freigegebener Produkte oder Produktvarianten 
 
Verwenden Sie die folgenden Kriterien, um die freigegebenen Produkte und Produktvarianten auszuwählen und zu aktualisieren: 

-    Der Produktlebenszyklusstatus des Produkts oder der Produktvariante muss sich vom neuen erwünschten Status unterscheiden. 
-  Das Produkt oder die Produktvariante wurde vor mehreren Tagen erstellt, basierend auf der Anzahl von Tagen, die Sie im Auswahldialogfeld eingeben. 
-  Es gibt keine offenen Produktionsaufträge (= Status < beendet) für das Produkt oder die Produktvariante. 
-  Es gibt keine offenen Lagerbuchungen (= Statusabgang „ReservPhysical” zu „QuotationIssue” oder Statuszugang „Registered” zu „QuotationReceipt”) für das Produkt oder die Produktvariante. 
-  Es gibt keine Lagerbuchungen innerhalb der letzten Anzahl von Tagen für das Produkt oder die Produktvariante. 
-  Es gibt keinen zukünftigen Bedarf oder Beschaffungsplanung für das Produkt oder die Produktvariante.  
-  Kein Minimaler Lagerbestand wurde in der Artikeldeckung für das Produkt oder die Produktvariante festgelegt. 
-  Keine aktive Kanbanregel für feste Menge für das Produkt oder die Produktvariante.  
-  Keine Serviceauftragsposition für das Produkt oder die Produktvariante. 
-  Keine aktiven oder zukünftigen Kaufvertrags- oder Bestellpositionen für das Produkt oder die Produktvariante. 
-  Das Produkt oder die Produktvariante wird nicht in einer Stückliste verwendet, die einer nicht abgelaufenen, genehmigten Stücklistenversion für ein Produkt oder eine Variante zugeordnet ist, das/die für die Planung aktiv ist.

## <a name="related-topics"></a>Verwandte Themen

-  Erstellen eines neuen Produktlebenszyklusstatus
-  Erstellen eines standardmäßigen neuen Produktlebenszyklusstatus
-  Ein Produktlebensyklusstatus einem freigegebenen Produktmaster zuweisen
-  Ein Produktlebensyklusstatus einem freigegebenen Produkt zuweisen
-  Veraltete Produktvarianten finden und ein Produktlebenszyklusstatus zuweisen
-  Ein Produktlebenszyklusstatus erstellen, um Produkte vom Produktprogrammplan auszuschließen

