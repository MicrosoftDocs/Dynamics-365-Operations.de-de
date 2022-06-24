---
title: Daten einer Tochtergesellschaft in Dateien exportieren
description: In diesem Artikel wird erläutert, wie Sie den Export von Daten aus Microsoft Dynamics 365 Finance vorbereiten und sie anschließend in eine konsolidierte juristische Person importieren.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 7c5334e206d28a5ae1c8097db5356cd1057b7180
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876152"
---
# <a name="export-subsidiary-data-to-files"></a>Daten einer Tochtergesellschaft in Dateien exportieren

[!include [banner](../includes/banner.md)]

Verwenden Sie die **Exportieren**-Seite (**Systemverwaltung \> Arbeitsbereiche \> Importieren/Exportieren**) zur Vorbereitung des Exports von Daten einer Tochtergesellschaft in Dateien, die dann in eine konsolidierte juristische Person importiert werden können. Weitere Informationen über die Import- und Exportprozesse finden Sie unter [Übersicht über Einzelvorgänge für Datenimport und ‑export](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

1. Erstellen Sie eine juristische Person für den Konsolidierungsprozess. Informationen zum Erstellen juristischer Personen finden Sie unter [Eine juristische Person erstellen](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Weitere Informationen finden Sie unter [Eine juristische Person für den Konsolidierungsprozess vorbereiten](prepare-company-for-consolidation.md) und [Eine juristische Person vom Typ Tochtergesellschaft zur Konsolidierung einrichten](set-up-subsidiary-company-for-consolidation.md). 

2. Rufen Sie **Konsolidierungen \> Unternehmenssalden exportieren** auf. Geben Sie auf der Registerkarte **Kriterien** der Seite **Unternehmenssalden exportieren** die Details der Konsolidierung an, indem Sie die folgenden Felder festlegen.

    | Feld                             | Beschreibung |
    |-----------------------------------|-------|
    | Hauptkonto                      | Geben Sie die zu konsolidierenden Konten an. Lassen Sie dieses Feld leer, um alle Konten einzuschließen. |
    | Konsolidierungskonto verwenden         | Wenn Sie Konsolidierungskonten angegeben haben, setzen Sie diese Option auf **Ja**. |
    | Konsolidierungskonto auswählen aus | Wählen Sie entweder **Hauptkonto** oder **Konsolidierungskontengruppe** aus. |
    | Konsolidierungskontogruppe       | Wählen Sie eine Konsolidierungskontengruppe für das ausgewählte Konsolidierungskonto aus. |
    | Konsolidierungsperiode              | Geben Sie einen „Von – Bis“–Datumsbereich für die Konsolidierung an. |
    | Istbeträge einbeziehen            | Setzen Sie diese Option auf **Ja**, um tatsächliche Beträge einzuschließen. |
    | Budgetbeträge einbeziehen            | Setzen Sie diese Option auf **Ja**, um Budgetbeträge in Konsolidierungen einzuschließen. |
    | Budgetmodelle                     | Geben Sie das einzuschließende Budgetmodell an. |

3. Geben Sie auf der Registerkarte **Finanzdimensionen** die Details der Konsolidierung an:

    - Geben Sie die Informationen zu den Finanzdimensionen an, die aus den Buchungen in den Konten der Tochtergesellschaften in die Buchungen der konsolidierten juristischen Person übertragen werden sollen.
    - Wählen Sie die Finanzdimensionen in der Liste aus.
    - Identifizieren Sie die richtige Spezifikation für jede konsolidierte Finanzdimension. Die verfügbaren Optionen umfassen **Dimension**, **Gruppendimension**, **Unternehmenskonten** und **Konto**.

        > [!NOTE]
        > Mithilfe der Option **Gruppendimension** können Sie den Dimensionswert definieren, der von der Unternehmensgruppe verwendet wird, die konsolidiert wird.

    - Geben Sie die Segmentreihenfolge an, in der konsolidiert werden soll.

4. Führen Sie die folgenden Schritte auf der Registerkarte **Juristische Personen** aus, um die zu exportierende juristische Person anzugeben:

    1. Wählen Sie **Neu** aus.
    2. Geben Sie im Feld **Juristische Person der Quelle** die juristische Person ein.

        Gelten für mehrere Tochtergesellschaften, die sich in derselben Datenbank befinden, die gleichen Kriterien, können Sie die Daten dieser Tochtergesellschaften in einem einzigen Schritt in verschiedene Exportdateien übertragen:

        1. Erstellen Sie für jede Tochtergesellschaft, deren Konten in Dateien exportiert werden sollen, eine Position. Diese Dateien werden später in die konsolidierte juristische Person importiert.
        2. Geben Sie für jede Tochtergesellschaft den Namen der Tochtergesellschaft sowie den Namen der Exportdatei ein, die im Zuge des Exportvorgangs erstellt wird.

    3. Wählen Sie im Feld **Kontenart für Konvertierungsdifferenzen** die Option **Gewinn und Verlust** oder **Bilanz** aus.
    4. Geben Sie einen Dateinamen für die zu erstellende Exportdatei ein.

5. Wählen Sie zum Ausführen des Exports **OK** aus.

Nach Abschluss des Exports erhalten Sie eine Meldung mit der Anzahl der in den einzelnen Dateien gespeicherten Datensätze. Sie können die Dateien dann in die konsolidierte juristische Person importieren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
