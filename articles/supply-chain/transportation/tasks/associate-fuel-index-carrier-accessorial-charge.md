---
title: Brennstoffindex einem Spediteur als Zusatzgebühr zuordnen
description: Dieses Handbuch, zeigt wie Sie eine Zusatzleistungszuweisung, Spediteurzusatzgebühr sowie einen Zusatzleistungsmaster für Benzinzuschlag erstellen und einen Spediteurskraftstoffindex einem Spediteur zuordnen.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1f69a6350a5a84ed19dcb37e174c25b112c16bd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974134"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>Brennstoffindex einem Spediteur als Zusatzgebühr zuordnen

[!include [banner](../../includes/banner.md)]

Dieses Handbuch, zeigt wie Sie eine Zusatzleistungszuweisung, Spediteurzusatzgebühr sowie einen Zusatzleistungsmaster für Benzinzuschlag erstellen und einen Spediteurskraftstoffindex einem Spediteur zuordnen. Sie müssen einen Spediteurskraftstoffindex eingerichtet haben, bevor Sie dieses Handbuch ausführen. Sie können das Handbuch „Einrichten eines Spedituerkraftstoffindex“ für diese Aufgaben verwenden. Diese Einrichtungsaufgaben werden normalerweise von einem Logistikmanager durchgeführt. Die Demodaten, die verwendet werden, um diese Prozedur zu erstellen, sind USMF.


## <a name="create-an-accessorial-master"></a>Erstellen eines Zusatzleistungsmaster
1. Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Bewertung" > "Zusatzleistungsmaster".
2. Klicken Sie auf "Neu".
3. Geben Sie einen Wert in das Feld "Zusatzleistungsmaster" ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Klicken Sie auf "Speichern".

## <a name="create-a-carrier-accessorial-charge"></a>Spediteurzusatzgebühr erstellen
1. Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Bewertung" > "Spediteurzusatzgebühren".
2. Klicken Sie auf "Neu".
3. Geben Sie einen Wert in das Feld "Spediteurzusatzleistungs-Kennung" ein.
4. Klicken Sie im Feld "Spediteur " auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * In diesem Beispiel wählen Sie LKW-Spediteur aus.  
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Klicken Sie im Feld "Spediteurdienstleistung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Klicken Sie im Feld "Zusatzleistungsmaster" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
10. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * In diesem Beispiel wählen Sie den neu erstellten Zusatzleistungsmaster aus.  
11. Klicken Sie auf "Speichern".

## <a name="create-an-accessorial-assignment"></a>Erstellen einer Zusatzleistungszuweisung
1. Klicken Sie auf "Zusatzleistungszuweisungen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein.
4. Schalten Sie die Erweiterung des Abschnitts "Kriterien" ein/aus.
    * In den Kriterien können Sie festlegen, dass der Benzinzuschlag immer angewendet wird, oder für dieses Beispiel wählen Sie aus, dass es nur innerhalb einer bestimmten Region gilt.  
5. Geben Sie im Feld "Postleitzahl Absender" einen Wert ein.
6. Geben Sie im Feld "Postleitzahl Empfänger" einen Wert ein.
7. Schalten Sie die Erweiterung des Abschnitts "Berechnung" ein/aus.
    * Im Berechnungsabschnitt können Sie angeben, wie der Benzinzuschlag berechnet wird. Diese Berechnung hängt von der Zusatzleistungseinheit ab, die Sie als Grundlage für die Berechnung ausgewählt haben.  
8. Wählen Sie im Feld "Gebührentyp Zusatzleistung" "Benzinzuschlag"aus.
9. Wählen Sie im Feld "Zusatzleistungseinheit" "Kilometerleistung" aus.
10. Klicken Sie im Feld "Region" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
12. Klicken Sie auf "Speichern".

## <a name="update-the-carrier-rating-profile"></a>Spediteurbewertungsprofil aktualisieren
1. Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Spediteure" > "Spediteure".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Schalten Sie die Erweiterung des Abschnitts "Bewertungsprofile" ein/aus.
4. Klicken Sie auf Bearbeiten.
5. Klicken Sie im Feld "Spediteur-Kraftstoffindex" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Klicken Sie auf "Speichern".

