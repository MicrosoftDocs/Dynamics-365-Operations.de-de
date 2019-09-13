---
title: Kaufvertrag erstellen
description: Dieses Thema führt Sie durch die Erstellung eines Kaufvertrags.
author: mkirknel
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec792ca27bf0245ff25e59cfe28122f17caec7fc
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866849"
---
# <a name="create-a-purchase-agreement"></a>Kaufvertrag erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Thema führt Sie durch die Erstellung eines Kaufvertrags. Dadurch wird normalerweise von einem Einkaufsleiter bearbeitet. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden. Sie müssen Einstellungen Kaufvertragsklassifizierungen haben, bevor Sie beginnen. Sobald Sie eine Vereinbarung erstellt haben, können Sie diese verwenden, wenn Sie eine Bestellung erstellen, und dieses kopiert die Kaufvertragszustände in den Kopf und alle möglichen Positionen in der Reihenfolge angezeigt, die in der Vereinbarung betroffen sind.


## <a name="create-a-new-purchase-agreement"></a>Erstellen Sie eine neue Rahmenbestellung
1. Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Kaufverträge > Kaufverträge**.
2. Klicken Sie auf **Neu**.
3. Wählen Sie im Feld **Kreditorenkonto** das Dropdownmenü aus und wählen Sie die Zeile des gewünschten Datensatzes aus.
4. Wählen Sie im Feld **Kaufvertragsklassifizierung** das Dropdownmenü aus und wählen Sie die Zeile des gewünschten Datensatzes aus.
5. Erweitern Sie das Inforegister **Allgemein**.
6. Geben Sie im Feld **Ablaufdatum** ein Datum ein.

    - Dieses Ablaufdatum ist der Standardwert für alle Zusagepositionen und bestimmt, wie lange jede einzelne Zusage gültig ist.  

7. Geben Sie im Feld **Dokumenttitel** einen Namen für den neuen Kaufvertrag ein.

    - Lassen Sie das Feld **Standardzusage** festgelegt auf **Produktmengenzusage** (oder ändern Sie es, wenn es noch nicht darauf festgelegt ist).  
    - Der standardmäßige Zusagewert bestimmt Die verfügbaren Optionen in der Vertragspositionen. Wenn Sie einen neuen Zusagetyp erfordern, wenn Sie die Vereinbarungspositionen erstellen, müssen Sie die standardmäßige Zusage im Kopf ändern. Es gibt 4 Typen von Zusagen: **Produktmengenzusage** – für eine bestimmte Menge eines Produkts; **Produktwertzusage** – für einen bestimmten Währungsbetrag eines Produkts; **Produktkategoriewertzusage** – für einen bestimmten Währungsbetrag in einer Beschaffungskategorie, in der der Betrag für einen Katalogartikel oder einen nicht im Katalog enthaltenen Artikel sein kann; **Wertzusage** – für einen bestimmten Währungsbetrag, der durch ein beliebiges Produkt oder von einer beliebigen Beschaffungskategorie gedeckt werden kann.  

8. Wählen Sie **OK**.

## <a name="add-a-commitment"></a>Zusage hinzufügen
1. Wählen Sie **Position hinzufügen** aus.
2. Wählen Sie im Feld **Artikelnummer** den gewünschten Datensatz aus dem Dropdown-Menü aus.
3. Geben Sie im Feld **Menge** eine Zahl ein. Dies ist die Gesamtmenge, die Sie Lieferscheinbuchung, von Ihrem Lieferanten kaufen.  
4. Geben Sie im Feld **Einzelpreis** eine Zahl ein.
5. Erweitern Sie den Abschnitt **Positionsdetails**.
6. Legen Sie die Option **Maximum wird erzwungen** auf **Ja** fest. Die Option **Maximum wird erzwungen** begrenzt die Verwendung der Zusage. Sie können nur bis zu der Menge einkaufen, die im Feld **Menge** für die Position angegeben ist.  

## <a name="add-header-conditions"></a>Kopfzeilenbedingungen hinzufügen
1. Wählen Sie im Aktivitätsbereich **Optionen** aus.
2. Wählen Sie **Ansicht wechseln** aus.
3. Wählen Sie **Kopfzeilenansicht** aus.
4. Erweitern Sie den Abschnitt **Bedingungen**.
5. Wählen Sie im Feld **Zahlungsmethode** den gewünschten Datensatz im Dropdownmenü aus. Die Zahlungsbedingungen vom Kreditorenkonto werden hier standardmäßig angezeigt.  
6. Wählen Sie im Feld **Lieferart** den gewünschten Datensatz im Dropdownmenü aus.
7. Wählen Sie im Feld **Lieferbedingungen** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.

## <a name="confirm-and-activate-the-agreement"></a>Bestätigen und Aktivieren des Kaufvertrags
1. Wählen Sie im Aktivitätsbereich **Kaufvertrag** aus.
2. Wählen Sie **Bestätigung** aus. Setzen Sie die Option **Vertrag als 'Effektiv' kennzeichnen** auf **Ja** fest.  
3. Wählen Sie **OK**.
4. Wählen Sie im Aktivitätsbereich **Kaufvertrag** aus.
5. Wählen Sie **Kaufvertragsbestätigungen** aus. Die Option **Vorschau anzeigen/Drucken** ermöglicht es Ihnen, ein Dokument für den Kaufvertrag zu generieren, den Sie an den Kreditor senden oder für diesen drucken können. Wenn Sie die Vereinbarung später aktualisieren und sie wieder-bestätigen, werden beide Versionen hier angezeigt.  
6. Schließen Sie die Seite.

