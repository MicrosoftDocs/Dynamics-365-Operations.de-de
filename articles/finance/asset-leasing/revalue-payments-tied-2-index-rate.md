---
title: An eine Indexrate gebundene Mietzahlungen neu bewerten
description: In diesem Artikel wird die Regulierung beschrieben, die an der Mietverbindlichkeit für eine Anlage mit Nutzungsrecht am Leasingobjekt vorgenommen wird, wenn sich die variablen Mietzahlungen aufgrund einer Änderung des Indexsatzes ändern.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8dc2325e9f0651bea0d70d9f66e5d88b741009f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903246"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a>An eine Indexrate gebundene Mietzahlungen neu bewerten

[!include [banner](../includes/banner.md)]

In diesem Artikel wird die Regulierung beschrieben, die an der Leasingverbindlichkeit für eine Anlage mit Nutzungsrecht am Leasingobjekt vorgenommen wird, wenn sich die variablen Mietzahlungen aufgrund einer Änderung des Indexsatzes ändern. Die Leasingverbindlichkeit und das Nutzungsrecht am Leasingobjekt werden angepasst, um die neuen Zahlungsbeträge zu berücksichtigen. Unter dem Kodifizierungsthema 842 (ASC 842) für Rechnungslegungsstandards, dem Standard für Generally Accepted Accounting Principles in den USA (US GAAP), ändern sich nur die variablen Zahlungen, wenn die Zahlungen aufgrund einer Änderung des Indexsatzes steigen oder fallen, sofern keine zusätzlichen Änderungen der Zahlungsströme vorhanden sind. Diese zusätzlichen Änderungen können eine Änderung der Mietdauer beinhalten, die sich auf die Zinssätze bezieht. Weitere Informationen finden Sie in ASC 842-10-55-225 und in Paragraph 42 (b) des International Financial Reporting Standard 16 (IFRS 16).

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

Öffnen Sie den Zahlungsplan für einen Mietvertrag, um die Auswirkungen des Mietvertragsneubewertungsprozesses auf ASC 842-Mietverträge anzuzeigen. Auf der Seite werden nur die variablen Zahlungen angezeigt, die am oder nach dem Datum der Neubewertung aufgrund der Neubewertung des Index vorgenommen wurden. Die Amortisierungs- und Abschreibungspläne bleiben unverändert. Wenn Sie eine Rechnung mit variabler Zahlung erstellen, wird die variable Zahlung dem Buchungskonto für variable Zahlungen belastet. Je nach den Einstellungen des Mietvertragsbuchs wird auch der variable Zahlungsbetrag zum Haben hinzugefügt, die direkt an den Lieferanten oder auf das Kreditorenkonto gebucht wird.

Die Zahlungsplanzeilen auf der Seite mit den Mietvertragsdetails werden automatisch mit einer neuen Zeile aktualisiert, die den neuen Indexsatz angibt. Darüber hinaus zeigt eine Spalte an, ob die Zeile manuell oder durch den Indexneubewertungsprozess erstellt wurde.

## <a name="ifrs-16-leases--index-revaluation"></a>IFRS 16-Mietverträge – Neubewertung des Index

Öffnen Sie die Mietvertragsdetails für einen angepassten Mietvertrag, um die Auswirkungen des Mietvertragsneubewertungsprozesses auf IFRS 16-Mietverträge anzuzeigen. Die Felder **Vertragslaufzeit** und **Nutzungsdauer der Anlage** wurden aktualisiert, um den Zeitablauf vom Beginn oder Änderungsdatum bis zum Neubewertungsdatum widerzuspiegeln. Darüber hinaus wurden die Zahlungsplanzeilen aktualisiert, um die neuen Zahlungen für den Mietvertrag, den neuen Indexsatz und die Art und Weise, wie die Zeile erstellt wurde, widerzuspiegeln.

Sie können den neu generierten Zahlungsplan anzeigen, der am Neubewertungsdatum beginnt, und den gesamten aktualisierten Zahlungsbetrag anzeigen. Ein neuer Tilgungsplan für Mietverbindlichkeiten und ein Abschreibungsplan für Vermögenswerte wurden ebenfalls erstellt, um den angepassten Zahlungsplan widerzuspiegeln.

Der Journaleintrag hat den Regulierungsjournaleintrag automatisch auf das Konto für die Änderung der Mietzahlungen gebucht, die mit der Indexneubewertung zusammenhängen.

> [!NOTE]
> Wenn die **Aufschlüsselungszahlungsbetrag**-Option auf dem **Allgemein**-Inforegister der **Mietdetails**-Seite aktiviert ist und das zugehörige Buch IFRS 16 ist, fügt der Index-Neubewertungsprozess automatisch einen Datensatz im **Zahlungsbetrag aufschlüsseln**-Dialogbox hinzu. Der Betrag spiegelt die Änderung wider, die aufgrund der Neubewertung des Index an der Zahlung vorgenommen wurde. Der Datensatz wird als **Wird für die Neubewertung des IRFS 16-Index verwendet** gekennzeichnet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
