---
title: Importieren der Daten einer Tochtergesellschaft aus Dateien
description: In diesem Thema wird erläutert, wie Sie Daten von externen Systemen so vorbereiten, dass sie in Microsoft Dynamics 365 Finance importiert werden können.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 0e122222e5d01d6616c1f1a9ce7c36f6aa901749
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826641"
---
# <a name="import-subsidiary-data-from-files"></a>Importieren der Daten einer Tochtergesellschaft aus Dateien

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Daten von externen Systemen so vorbereiten, dass sie in Microsoft Dynamics 365 Finance importiert werden können. Sie verwenden die **Mit Import konsolidieren**-Seite (**Konsolidierungen \> Mit Import konsolidieren**), um die Übertragung von Daten zu Tochtergesellschaften aus externen Systemen vorzubereiten.

1. Erstellen Sie eine juristische Person der Tochtergesellschaft für die Konsolidierung. Informationen zum Erstellen juristischer Personen finden Sie unter [Eine juristische Person erstellen](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Weitere Informationen finden Sie unter [Eine juristische Person für den Konsolidierungsprozess vorbereiten](prepare-company-for-consolidation.md) und [Eine juristische Person vom Typ Tochtergesellschaft zur Konsolidierung einrichten](set-up-subsidiary-company-for-consolidation.md).

2. Bereiten Sie eine Datei vor, die die importierten Daten enthält. Weitere Informationen über den Importprozess finden Sie unter [Übersicht über Einzelvorgänge für Datenimport und ‑export](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
3. Exportieren Sie die Daten in eine Datei, indem Sie die Schritte im Verfahren „Datenimport / -Export“ in [Übersicht über Datenimport- und -exportaufgaben](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) ausführen. Mit diesem Verfahren können Sie Daten aus einer anderen Dynamics 365 Finance-Instanz oder von Dynamics 365 Business Central konsolidieren . Wenn Sie Daten aus externen Systemen importieren, müssen die Daten das in [Exportieren von Daten von Tochtergesellschaften in Dateien](export-subsidiary-data-to-file.md) beschriebene Format haben.
4. Wechseln Sie zu **Konsolidierungen \> Mit Import konsolidieren**. Geben Sie auf der Seite **Mit Import konsolidieren** auf der Registerkarte **Kriterien** die Details des Bereichts und/oder des Imports ein, indem Sie die folgenden Felder festlegen.

    | Feld                                 | Wert für den Bericht | Wert für den Import |
    |---------------------------------------|----------------------|----------------------|
    | Beschreibung                           | Nicht zutreffend | Geben Sie eine Beschreibung zur Bestimmung des Imports ein. |
    | Hauptkonto                          | Definieren Sie den Kontenbereich, den der Bericht enthalten soll. Wenn Sie keinen Bereich definieren, werden alle Konten einbezogen. | Definieren Sie den Kontenbereich, den der Import enthalten soll. Wenn Sie keinen Bereich definieren, werden alle Konten einbezogen. |
    | Konsolidierungsperiode                  | Definieren Sie den zu konsolidierenden Datumsbereich. | Definieren Sie den zu konsolidierenden Datumsbereich. |
    | Istbeträge einbeziehen                | Setzen Sie diese Option auf **Ja**, um die Istwerte einzuschließen. | Setzen Sie diese Option auf **Ja**, um die Istwerte einzuschließen. |
    | Budgetbeträge einbeziehen                | Setzen Sie diese Option auf **Ja**, um Budgetbeträge in Konsolidierungen einzuschließen. | Setzen Sie diese Option auf **Ja**, um Budgetbeträge in Konsolidierungen einzuschließen. |
    | Guthaben während der Konsolidierung neu erstellen | Setzen Sie diese Option auf **Ja**, wenn der Wiederherstellungsprozess den Saldo und die neuen Datensätze vollständig löschen und den Saldo von Anfang an neu erstellen soll. | Setzen Sie diese Option auf **Ja**, wenn der Wiederherstellungsprozess den Saldo und die neuen Datensätze vollständig löschen und den Saldo von Anfang an neu erstellen soll. |
    | Budgetmodelle                         | Nicht zutreffend | Wenn Sie den Import von Budgetbeträgen ausgewählt haben, geben Sie die zu konsolidierenden Budgetmodelle ein. |
    | Budgetkurstyp                      | Nicht zutreffend | Geben Sie den Typ des Budget-Wechselkurses ein. |

6. Wenn Sie unterschiedliche Buchhaltungswährungen haben, verwenden Sie die Felder auf der **Währungsumrechnung**-Registerkarte, um die Umrechnung zu konfigurieren, die während der Konsolidierung durchgeführt wird.

    | Feld                      | Beschreibung |
    |----------------------------|-------------|
    | Juristische Quellperson        | Wählen Sie die juristische Person aus, von der Sie importieren. |
    | Buchhaltungswährung der Quellen | Diese Standardwährung ist die Währung, die der juristischen Quellperson zugeordnet ist, die Sie im **Juristische Person der Quelle**-Feld ausgewählt haben. |
    | Von- und Bis-Konten       | Definieren Sie den Bereich der aus der juristischen Quellperson zu importierenden Konten. |
    | Wechselkurstyp         | Wählen Sie den Typ des Wechselkurses aus. Wechselkurstypen werden beim Erstellen eines Hauptkontos zugewiesen. Weitere Informationen finden Sie unter [Erstellen eines Hauptkontos](tasks/create-main-account.md). |
    | Anwenden des Wechselkurses vom   | Geben Sie ein Datum ein, um den an diesem Datum gültigen Wechselkurs anzuwenden. Alternativ können Sie den Wert eingeben, der als Wechselkurs verwendet werden soll. |
    | Kurs              | Der Standardwert hängt vom Typ des Wechselkurses ab, den Sie im Feld **Wechselkurstyp** ausgewählt haben. Wenn Sie einen benutzerdefinierten Wechselkurs eingegeben haben, können Sie einen Kurs definieren. |

7. Stellen Sie die **Im Hintergrund ausführen**-Option auf **Ja**, damit der Importvorgang im Hintergrund ausgeführt werden kann.
8. Stellen Sie die **Stapelverarbeitung**-Option auf **Ja**, um die Konsolidierung zu einem bestimmten Zeitpunkt als Stapelaufgabe auszuführen. Um die Konsolidierung sofort auszuführen, wählen Sie **OK**. 

Die in den Tochtergesellschaften für die Konsolidierung angegebenen Buchungen und Salden werden den entsprechenden Konten der konsolidierten juristischen Person hinzugefügt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]