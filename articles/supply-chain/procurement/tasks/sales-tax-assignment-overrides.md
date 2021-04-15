---
title: Mehrwertsteuer-Zuweisung und -Außerkraftsetzungen
description: Diese Prozedur zeigt, wie Sie Handelskanälen Mehrwertsteuergruppen zuweisen.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 28d393dcf727eec7211f6092ea67de2b85359f1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811941"
---
# <a name="sales-tax-assignment-and-overrides"></a>Mehrwertsteuer-Zuweisung und -Außerkraftsetzungen

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie Sie Handelskanälen Mehrwertsteuergruppen zuweisen. Sie führt auch Schritt für Schritt durch den Prozess der Erstellung einer neuen Mehrwertsteuer-Außerkraftsetzung und ihrer Zuweisung zu einer vorhandenen Mehrwertsteuer-Außerkraftsetzungsgruppe. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Navigieren Sie zu Einzelhandel und Commerce > Kanäle > Geschäfte > Alle Einzelhandelsgeschäfte.
2. Klicken Sie in der Liste auf den Kanalkennungslink für „Houston“.
3. Klicken Sie auf Bearbeiten.
    * Das Feld "Mehrwertsteuergruppe" enthält eine Liste von Mehrwertsteuergruppen für das aktuelle Unternehmen. Die aktuell zugewiesene Gruppe ist eine generische Mehrwertsteuergruppe "Texas". Es gibt auch für Mehrwertsteuergruppen für "Washington" und "Washington, King County". Mehrwertsteuergruppen können entsprechende Steuern für mehrere Gemeinden enthalten.  
    * Im Feld "Mehrwertsteuer-Außerkraftsetzung" können Mehrwertsteuer-Außerkraftsetzungsgruppen dem Kanal zugeordnet werden. Mehrwertsteuer-Außerkraftsetzungsgruppen können verwendet werden, um Mehrwertsteuer-Außerkraftsetzungen zusammen zu gruppieren, die für mehrere Läden gelten. Anstatt Mehrwertsteuer-Außerkraftsetzungen manuell einzeln zuzuweisen, kann die Gruppe erstellt und direkt den Kanälen zugewiesen werden, um Zeit zu sparen.  
4. Klicken Sie auf Speichern.
5. Schließen Sie die Seite.
6. Wechseln Sie zu Retail und Commerce > Kanaleinrichtung > Mehrwertsteuern > Mehrwertsteuer-Außerkraftsetzungen.
7. Klicken Sie auf "Neu".
8. Geben Sie im Feld "Mehrwertsteuer-Außerkraftsetzung" einen Namen für Ihre neue Außerkraftsetzung an.
9. Geben Sie im Feld "Beschreibung" eine Beschreibung der Außerkraftsetzung an.
10. Legen Sie den Status auf "Aktivieren" fest.
11. Erweitern oder reduzieren Sie den Abschnitt "Außerkraftsetzung".
12. Wählen Sie im Feld "Typ" eine Option aus.
    * Artikel-Mehrwertsteuergruppen können verwendet werden, um Steuern für bestimmte Artikel außer Kraft zu setzen, die zur Gruppe gehören. Zum Beispiel werden Nahrungsmittel gewöhnlich anders als Gebrauchsgüter besteuert und sie haben mit hoher Wahrscheinlichkeit ihre eigene Mehrwertsteuergruppe. Mehrwertsteuergruppen sind Gruppen von Steuern, die für einen bestimmten Kanal gelten. Zum Beispiel wenn ein Kanal sowohl für den Einzelhandel verkauft als auch zwischen Unternehmen verkauft, werden möglicherweise unterschiedliche Artikel-Mehrwertsteuergruppen verwendet. Alle anwendbaren Steuern würden der Mehrwertsteuergruppe zugeordnet werden.  
    * Sie können jetzt die Steuern "Von" und "Bis" oder die "Von-Steuergruppe" und die "Bis-Steuergruppe" auswählen, um Ihre Mehrwertsteuer-Außerkraftsetzung zu erstellen. Das Feld "Von" zeigt die Steuer oder Steuergruppe an, die außer Kraft gesetzt werden soll. Die Außerkraftsetzung nach Artikel-Mehrwertsteuergruppe stellt andere Optionen bereit, als das Außerkraftsetzen nach Mehrwertsteuergruppe. Mehrwertsteuer-Außerkraftsetzungen können so eingerichtet werden, dass sie Steuern für gesamte Transaktionen oder für bestimmte Positionen in einer Transaktion außer Kraft setzen.  
13. Klicken Sie auf Speichern.
14. Schließen Sie die Seite.
15. Wechseln Sie zu Retail und Commerce > Kanaleinrichtung > Mehrwertsteuern > Mehrwertsteuer-Außerkraftsetzungsgruppen.
    * In diesem Schritt wird Ihnen die neu erstellte Mehrwertsteuer-Außerkraftsetzung zur Mehrwertsteuer-Außerkraftsetzungsgruppe zugewiesen werden, die dem Kanal "Houston" zugewiesen ist.  
16. Klicken Sie auf "Bearbeiten".
17. Erweitern oder reduzieren Sie den Abschnitt 'Einrichten'.
18. Klicken Sie auf Hinzufügen.
19. Klicken Sie im Feld "Mehrwertsteuer-Außerkraftsetzung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
20. Wählen Sie die vorher erstellte Mehrwertsteuer-Außerkraftsetzung von der Liste aus.
21. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
22. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]