---
title: Anforderung für Verbrauch erstellen
description: In diesem Thema wird der Prozess zum Erstellen einer Anforderung beschrieben.
author: mkirknel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2948282d8b40f7d34ffbae072a195cf954ab6e2
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/10/2019
ms.locfileid: "1738903"
---
# <a name="create-a-requisition-for-consumption"></a>Anforderung für Verbrauch erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Thema wird der Prozess zum Erstellen einer Anforderung beschrieben. Sie erfahren Ihnen unterschiedliche Arten an, für Produkte im Beschaffungskatalog zu suchen und wie ein Produkt hinzufügt, das nicht im Katalog ist. Überprüfen Sie zunächst, müssen Sie eine Einkaufsrichtlinieneinstellung mit der Verbrauch mit der Standardtyp der Anforderung offen. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden. Die Prozedur kann in einem Benutzerprofil nur ausgeführt werden, das als Arbeitskraft eingerichtet ist. Diese Aufgaben werden normalerweise von einem Lagerortmitarbeiter ausgeführt. Die Sicherheitsrolle **Mitarbeiter** ermöglicht es Ihnen, diese Aufgaben auszuführen. Sie können sich auch als **Alicia** anmelden, wenn Sie USMF verwenden.


## <a name="create-a-new-requisition"></a>Neue Reiseanforderung erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Bestellanforderungen > Von mir vorbereitete Bestellanforderungen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Name** einen Namen für die Anforderung ein.
4. Geben Sie im Feld **Angefordertes Datum** ein Datum ein. Hier werden das angeforderte Datum, der Abschlussstichtag und die Geschäftsbegründung für die Bestellanforderungsposition angezeigt. Sie können auch auf Positionsebene geändert werden. Das angeforderte Datum ist das angeforderte Lieferdatum.  
5. Geben Sie ein Datum in das Feld **Abschlussstichtag** ein. Der Abschlussstichtag wird zum Erfassen des Buchhaltungseintrags im Hauptbuch und zum Überprüfen der verfügbaren Budgetmittel verwendet.  
6. Wählen Sie **OK**.
7. Wählen Sie im Feld **Grund** eine Option in der Dropdownliste aus. Die ausgewählte geschäftliche Begründung wird standardmäßig für Bestellanforderungspositionen angezeigt, kann aber auf Positionsebene geändert werden.  
8. Wählen Sie den Grund aus.
9. Geben Sie im Feld **Details** eine aussagekräftigere Begründung für die Anforderung ein.

## <a name="add-a-line-to-the-requisition"></a>Fügt dem Arbeitszeitnachweis eine neue Zeile hinzu.
1. Wählen Sie **Position hinzufügen** aus. Es gibt zwei Möglichkeiten zum Hinzufügen von Positionen der Bestellanforderung. Wenn Sie die Produktnummer kennen oder bereits wissen, dass Sie ein Produkt anfordern, das sich nicht im Produktkatalog befindet, können Sie die Position direkt über **Position hinzufügen** hinzufügen. Die andere Möglichkeit besteht darin, **Produkte hinzufügen** zu verwenden. Hier können Sie nach Artikeln im Produktkatalog suchen und Filter anwenden.    
2. Wählen Sie die Zeile aus, die Sie soeben erstellt haben.
    - Die anfordernde Person ist die Arbeitskraft, die die Anforderung angefordert hat.   
    - Standardmäßig ist die Person, die die Anforderung vorbereitet, die Arbeitskraft, die sie angefordert hat. Sie müssen die Erlaubnis werden, eine Bestellanforderungsposition im Auftrag einer anderen Arbeitskraft vorbereitet. Wenn Sie solche Berechtigungen dann haben, zeigen andere Arbeitskräfte in dieser Suche.  
3. Geben Sie im Feld **Artikelnummer** einen Wert ein. Die Artikel, die verfügbar sind, damit Sie auswählen, werden durch die Kategoriezugriffsrichtlinie und den Beschaffungskatalog für die kaufende juristische Person beschränkt.   
4. Geben Sie im Feld **Menge** eine Zahl ein.

## <a name="add-more-products-to-the-requisition"></a>Produkte zu einer Bestellanforderung hinzufügen
1. Wählen Sie **Produkte hinzufügen** aus. Dies ist die Option, in der Sie für Produkte im Produktkatalog suchen können.    
2. Geben Sie im Feld **Beschaffungskategorieknoten suchen** den ersten Teil des Namens der Kategorie ein, nach der Sie suchen, und klicken Sie dann auf die**EINGABETASTE**. Geben Sie beispielsweise `comput` ein.  
3. Verwenden Sie die Verknüpfung **InvokeDefaultButton**.
4. Verwenden Sie den **Filter**, um die Liste der Produkte in der ausgewählten Kategorie zu filtern.
5. Wählen Sie hier die Produkte aus, die Sie der Bestellanforderung hinzufügen möchten.
6. Wählen Sie **Zu Positionen hinzufügen**.
7. Geben Sie im Feld **Menge** eine Zahl ein.
8. Geben Sie im Feld **Beschaffungskategorieknoten suchen** den ersten Teil des Namens der Kategorie ein, nach der Sie suchen, und klicken Sie dann auf die **EINGABETASTE**. Geben Sie für dieses Beispiel `High` (Textmarker) ein.  
9. Verwenden Sie die Verknüpfung **InvokeDefaultButton**.
10. Wählen Sie **Nicht gelistete Produkte zu Positionen hinzufügen** aus, um ein Produkt hinzuzufügen, das nicht im Beschaffungskatalog aufgeführt ist.
11. Geben Sie im Feld **Produktname** einen Wert ein.
12. Geben Sie im Feld **Einheit** einen Wert ein.
13. Wählen Sie **OK**.
14. Geben Sie im Feld **Artikelbeschreibung** eine Beschreibung des Produkts ein.
15. Geben Sie im Feld **Menge** eine Zahl ein.
16. Geben Sie im Feld **Einzelpreis** eine Zahl ein. Wenn Sie den Preis für einen bestimmten Kreditor (den Sie im Feld „Kreditorenkonto“ auswählen) kennen, kann dieser Preis eingegeben werden.   
17. Öffnen Sie im Feld **Kreditorenkonto** die Dropdownliste, um eine Option auszuwählen. Kreditoren, die in diesem Feld verfügbar sind, hängt von den Einkaufsrichtlinien und vom Status ab, den der Kreditor für die aktuelle Beschaffungskategorie hat. Als Alternative zur Auswahl eines Kreditors an dieser Stelle können Sie auch **Kreditoren vorschlagen** auswählen.    
18. Wählen Sie in der Liste die Arbeitskraft aus, die Sie verwenden möchten.
19. Geben Sie im Feld **Externe Artikelnummer** einen Wert ein. Dies ist eine Referenznummer für das Produkt, das vom Kreditor bekannt ist. Beispielsweise kann diese die Artikelnummer des Produkts im eigenen Katalog des Kreditors sein.  
20. Wählen Sie **OK**.

## <a name="distribute-amounts"></a>Beträge verteilen
1. Wählen Sie **Finanzdaten** aus.
2. Wählen Sie **Beträge verteilen** aus. Dieser Prozess zeigt Ihnen an, wie die Kosten für die erste Position zwischen 2 Konten verteilt. Dies kann auch später nachholen, wenn die Anforderung im geprüft.  
3. Wählen Sie **Teilen** aus, um eine neue Verteilungsposition zu erstellen.
4. Wählen Sie im Feld **Sachkonto** die erste Kostenstelle, die sich an den Kosten beteiligen soll.
5. Löschen Sie die ausgewählte Verteilungsposition.
6. Geben Sie im Feld "Konto für Sachkontobuchungen" die gewünschten Werte an.
7. Wählen Sie **Gleichmäßig verteilen** aus.
8. Schließen Sie die Seite.

## <a name="view-line-details"></a>Artikel-Details anzeigen
1. Schalten Sie die Erweiterung des Abschnitts **Positionsdetails** ein/aus.

## <a name="submit-the-requisition"></a>Materialanforderung übermitteln
1. Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf **Workflow**.
2. Wählen Sie **Senden**.
3. Schließen Sie die Seite.
4. Geben Sie im Feld **Kommentar** einen Hinweis für den Genehmiger der Anforderung ein.
5. Wählen Sie **Senden**.
6. Schließen Sie die Seite.
7. Aktualisieren Sie die Seite.

