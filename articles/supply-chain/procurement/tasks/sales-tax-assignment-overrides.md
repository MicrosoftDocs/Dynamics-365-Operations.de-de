--- 
title: "Mehrwertsteuer-Zuweisung und -Außerkraftsetzungen"
description: Diese Prozedur zeigt, wie man Mehrwertsteuergruppen Retail Channels zuweist.
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 816e00e4238cb0d90a2aea9b2bc070d31504c2ce
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="sales-tax-assignment-and-overrides"></a>Mehrwertsteuer-Zuweisung und -Außerkraftsetzungen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie man Mehrwertsteuergruppen Retail Channels zuweist. Sie führt auch Schritt für Schritt durch den Prozess der Erstellung einer neuen Mehrwertsteuer-Außerkraftsetzung und ihrer Zuweisung zu einer vorhandenen Mehrwertsteuer-Außerkraftsetzungsgruppe. Diese Prozedur

nutzt das USRT Unternehmen in den Demodaten.

1. Navigieren Sie zu Einzelhandel und Handel > Kanäle > Einzelhandelsgeschäfte > Alle Einzelhandelsgeschäfte.
2. In der Liste klicken Sie auf Retail Channel-Kennungslink für "Houston".
3. Klicken Sie auf "Bearbeiten".
    * Das Feld "Mehrwertsteuergruppe" enthält eine Liste von Mehrwertsteuergruppen für das aktuelle Unternehmen. Die aktuell zugewiesene Gruppe ist eine generische Mehrwertsteuergruppe "Texas". Es gibt auch für Mehrwertsteuergruppen für "Washington" und "Washington, King County". Mehrwertsteuergruppen können entsprechende Steuern für mehrere Gemeinden enthalten.  
    * Im Feld "Mehrwertsteuer-Außerkraftsetzung" können Mehrwertsteuer-Außerkraftsetzungsgruppen dem Kanal zugeordnet werden. Mehrwertsteuer-Außerkraftsetzungsgruppen können verwendet werden, um Mehrwertsteuer-Außerkraftsetzungen zusammen zu gruppieren, die für mehrere Läden gelten. Anstatt Mehrwertsteuer-Außerkraftsetzungen manuell einzeln zuzuweisen, kann die Gruppe erstellt und direkt den Kanälen zugewiesen werden, um Zeit zu sparen.  
4. Klicken Sie auf "Speichern".
5. Schließen Sie die Seite.
6. Wechseln Sie zu "Einzelhandel und Handel" > "Kanaleinrichtung" > "Mehrwertsteuern" > "Mehrwertsteuer-Außerkraftsetzungen".
7. Klicken Sie auf "Neu".
8. Geben Sie im Feld "Mehrwertsteuer-Außerkraftsetzung" einen Namen für Ihre neue Außerkraftsetzung an.
9. Geben Sie im Feld "Beschreibung" eine Beschreibung der Außerkraftsetzung an.
10. Legen Sie den Status auf "Aktivieren" fest.
11. Erweitern oder reduzieren Sie den Abschnitt "Außerkraftsetzung".
12. Wählen Sie im Feld "Typ" eine Option aus.
    * Artikel-Mehrwertsteuergruppen können verwendet werden, um Steuern für bestimmte Artikel außer Kraft zu setzen, die zur Gruppe gehören. Zum Beispiel werden Nahrungsmittel gewöhnlich anders als Gebrauchsgüter besteuert und sie haben mit hoher Wahrscheinlichkeit ihre eigene Mehrwertsteuergruppe.     Mehrwertsteuergruppen sind Gruppen von Steuern, die für einen bestimmten Kanal gelten. Zum Beispiel wenn ein Kanal sowohl für den Einzelhandel verkauft als auch zwischen Unternehmen verkauft, werden möglicherweise unterschiedliche Artikel-Mehrwertsteuergruppen verwendet. Alle anwendbaren Steuern würden der Mehrwertsteuergruppe zugeordnet werden.  
    * Sie können jetzt die Steuern "Von" und "Bis" oder die "Von-Steuergruppe" und die "Bis-Steuergruppe" auswählen, um Ihre Mehrwertsteuer-Außerkraftsetzung zu erstellen.    Das Feld "Von" zeigt die Steuer oder Steuergruppe an, die außer Kraft gesetzt werden soll. Die Außerkraftsetzung nach Artikel-Mehrwertsteuergruppe stellt andere Optionen bereit, als das Außerkraftsetzen nach Mehrwertsteuergruppe.    Mehrwertsteuer-Außerkraftsetzungen können so eingerichtet werden, dass sie Steuern für gesamte Transaktionen oder für bestimmte Positionen in einer Transaktion außer Kraft setzen.  
13. Klicken Sie auf "Speichern".
14. Schließen Sie die Seite.
15. Wechseln Sie zu "Einzelhandel und Handel" > "Kanaleinrichtung" > "Mehrwertsteuern" > "Mehrwertsteuer-Außerkraftsetzungsgruppen".
    * In diesem Schritt wird Ihnen die neu erstellte Mehrwertsteuer-Außerkraftsetzung zur Mehrwertsteuer-Außerkraftsetzungsgruppe zugewiesen werden, die dem Kanal "Houston" zugewiesen ist.  
16. Klicken Sie auf "Bearbeiten".
17. Erweitern oder reduzieren Sie den Abschnitt 'Einrichten'.
18. Klicken Sie auf Hinzufügen.
19. Klicken Sie im Feld "Mehrwertsteuer-Außerkraftsetzung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
20. Wählen Sie die vorher erstellte Mehrwertsteuer-Außerkraftsetzung von der Liste aus.
21. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
22. Klicken Sie auf "Speichern".


