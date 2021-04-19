---
title: An eine Indexrate gebundene Mietzahlungen neu bewerten
description: In diesem Thema wird die Regulierung beschrieben, die an der Mietverbindlichkeit für eine Anlage mit Nutzungsrecht am Leasingobjekt vorgenommen wird, wenn sich die variablen Mietzahlungen aufgrund einer Änderung des Indexsatzes ändern.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8d743bb51cfc1487e76ee46adfd59276f1c1b48b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819721"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a>An eine Indexrate gebundene Mietzahlungen neu bewerten

[!include [banner](../includes/banner.md)]

In diesem Thema wird die Regulierung beschrieben, die an der Mietverbindlichkeit für eine Anlage mit Nutzungsrecht am Leasingobjekt vorgenommen wird, wenn sich die variablen Mietzahlungen aufgrund einer Änderung des Indexsatzes ändern. Die Leasingverbindlichkeit und das Nutzungsrecht am Leasingobjekt werden angepasst, um die neuen Zahlungsbeträge zu berücksichtigen. Unter dem Kodifizierungsthema 842 (ASC 842) für Rechnungslegungsstandards, dem Standard für Generally Accepted Accounting Principles in den USA (US GAAP), ändern sich nur die variablen Zahlungen, wenn die Zahlungen aufgrund einer Änderung des Indexsatzes steigen oder fallen, sofern keine zusätzlichen Änderungen der Zahlungsströme vorhanden sind. Diese zusätzlichen Änderungen können eine Änderung der Mietdauer beinhalten, die sich auf die Zinssätze bezieht. Weitere Informationen finden Sie in ASC 842-10-55-225 und in Paragraph 42 (b) des International Financial Reporting Standard 16 (IFRS 16).

## <a name="adjust-lease-payments"></a>Mietzahlungen anpassen

Führen Sie diese Schritte aus, um an eine Indexrate gebundene Mietzahlungen neu bewerten.

1. Um den Neubewertungsprozess für den Mietindex auszuführen, gehen Sie zu **Anlagenleasing \> Periodisch \> Neubewertung des Indexsatzes**.

    Die Seite **Neubewertung des Indexsatzes** wird angezeigt und zeigt alle vorherigen Mietindex-Neubewertungsprozesse an, die ausgeführt wurden. Zu den Informationen auf dieser Seite gehören die Prozess-ID, die aus der Einrichtung der Nummernfolge generiert wurde, die juristische Person, die Anzahl der angepassten Leasingbücher, die gesamte Verbindlichkeitsregulierung für IFRS 16-Mietverträge und die gesamten variablen Zahlungen, die für ASC 842-Mietverträge angepasst wurden.

2. Um die Neubewertung auszuführen, wählen Sie im Aktionsbereich **Neubewertung des Mietindex** aus.

    Das Dialogfeld **Parameter zur Neubewertung des Index** wird angezeigt. Hier können Sie filtern und auswählen, welche Mietverträge, Mietgruppen oder andere Kriterien verwendet werden sollen, wenn Sie die Mietverträge auswählen, die neu bewertet werden sollen. Zusätzlich können Sie auf der **Im Hintergrund ausführen**-Registerkarte den Indexneubewertungsprozess so einrichten, dass er in einem Batch ausgeführt wird.

4. Wählen Sie die Filter für die Auswahl von Mietverträgen aus, die in die Hintergrundverarbeitung einbezogen werden sollen, und wählen Sie dann **OK**.

    Das Dialogfeld **Vorschau der Neubewertung der Indexrate** wird angezeigt und zeigt die Mietverträge an, die neu bewertet werden. Es werden auch die Aktiva und Passiva-Anpassungen oder die variablen Zahlungsanpassungen angezeigt.
    
5. Wählen Sie die Mietverträge aus, um zu verhindern, dass Mietverträge neu bewertet werden, die neu bewertet werden **sollten**. Wenn Sie keine Mietverträge auswählen, werden alle Mietverträge neu bewertet. Wenn Sie fertig sind, wählen Sie **OK** aus, um die Mietzahlungen neu zu bewerten.
6. Um die Transaktionen anzuzeigen, die für einen bestimmten Indexneubewertungsprozess erstellt wurden, wählen Sie die Prozess-ID aus und wählen Sie dann **Transaktionen**.

    Ein Dialogfeld wird angezeigt und zeigt die Details der Transaktionen an, die während der Verarbeitung erstellt wurden.

> [!NOTE]
> Nur Mietverträge mit einem Neubewertungsdatum, das am oder vor dem Systemdatum liegt, können neu bewertet werden. Das System ignoriert automatisch alle Mietverträge mit einem Neubewertungsdatum, das nach dem Systemdatum liegt.

## <a name="asc-842-leases--index-revaluation"></a>ASC 842-Mietverträge – Neubewertung des Index

Öffnen Sie den Zahlungsplan für einen Mietvertrag, um die Auswirkungen des Mietvertragsneubewertungsprozesses auf ASC 842-Mietverträge anzuzeigen. Auf der Seite werden nur die variablen Zahlungen angezeigt, die am oder nach dem Datum der Neubewertung aufgrund der Neubewertung des Index vorgenommen wurden. Die Amortisierungs- und Abschreibungspläne bleiben unverändert. Wenn Sie eine Rechnung mit variabler Zahlung erstellen, wird die variable Zahlung dem Buchungskonto für variable Zahlungen belastet. Je nach Einrichtung des Mietvertragsbuchs wird auch der variable Zahlungsbetrag zu der Gutschrift hinzugefügt, die direkt an den Lieferanten oder auf das Kreditorenkonto gebucht wird.

Die Zahlungsplanzeilen auf der Seite mit den Mietvertragsdetails werden automatisch mit einer neuen Zeile aktualisiert, die den neuen Indexsatz angibt. Darüber hinaus zeigt eine Spalte an, ob die Zeile manuell oder durch den Indexneubewertungsprozess erstellt wurde.

## <a name="ifrs-16-leases--index-revaluation"></a>IFRS 16-Mietverträge – Neubewertung des Index

Öffnen Sie die Mietvertragsdetails für einen angepassten Mietvertrag, um die Auswirkungen des Mietvertragsneubewertungsprozesses auf IFRS 16-Mietverträge anzuzeigen. Die Felder **Vertragslaufzeit** und **Nutzungsdauer der Anlage** wurden aktualisiert, um den Zeitablauf vom Beginn oder Änderungsdatum bis zum Neubewertungsdatum widerzuspiegeln. Darüber hinaus wurden die Zahlungsplanzeilen aktualisiert, um die neuen Zahlungen für den Mietvertrag, den neuen Indexsatz und die Art und Weise, wie die Zeile erstellt wurde, widerzuspiegeln.

Sie können den neu generierten Zahlungsplan anzeigen, der am Neubewertungsdatum beginnt, und den gesamten aktualisierten Zahlungsbetrag anzeigen. Ein neuer Tilgungsplan für Mietverbindlichkeiten und ein Abschreibungsplan für Vermögenswerte wurden ebenfalls erstellt, um den angepassten Zahlungsplan widerzuspiegeln.

Der Journaleintrag hat den Regulierungsjournaleintrag automatisch auf das Konto für die Änderung der Mietzahlungen gebucht, die mit der Indexneubewertung zusammenhängen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]