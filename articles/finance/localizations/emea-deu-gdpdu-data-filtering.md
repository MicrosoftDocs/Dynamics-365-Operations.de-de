---
title: Hinzufügen von Filtern zu einer Audit-Datei-Konfiguration
description: In diesem Artikel wird erklärt, wie Sie einen Datenfilter in der deutschen Protokolldatei hinzufügen können.
author: AdamTrukawka
ms.date: 02/09/2021
ms.topic: article
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Germany
ms.author: atrukawk
ms.search.form: ERWorkspace
ms.openlocfilehash: 0d1bbafc822e9da2f14673d2fe24b8c5dc263d4f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287844"
---
# <a name="add-filters-to-an-audit-file-configuration"></a>Hinzufügen von Filtern zu einer Audit-Datei-Konfiguration

[!include [banner](../includes/banner.md)]

Dieser Artikel erklärt, wie Sie einen Filter für Daten in der deutschen Protokolldatei hinzufügen können. Sie können zum Beispiel einen Filter für das Feld **Buchungsebene** in der Tabelle **Allgemeiner Erfassungseintrag** hinzufügen.

Wie in [Übersicht über die deutsche Prüfdatei (GDPdU/GoBD)](emea-deu-gdpdu-audit-data-export.md#sachkontobuchungen) erläutert, wird das Feld **SPEZIALBUCHUNG** (Buchungsschicht) des **Datensatzes Sachkontobuchungen** aus dem Datenquellenpfad **$GeneralJournalEntry/PostingLayer** für elektronische Meldungen gesammelt. Um die Möglichkeit hinzuzufügen, Daten im Bericht nach dem Feld **SPEZIALBUCHUNG** (Buchungsschicht) zu filtern, führen Sie die folgenden Schritte aus:

1. Gehen Sie zu **Arbeitsbereiche** > **Elektronisches Berichtswesen**, und wählen Sie dann **Berichtskonfigurationen**.
2. Wählen Sie im Konfigurationsbaum die Konfiguration **Datenexportmodell** und leiten Sie sie ab, indem Sie ein Format erstellen, das in Ihrer Firma verwendet wird.
3. Wählen Sie die abgeleitete Konfiguration aus und wählen Sie im Aktivitätsbereich **Designer**. 
4. Wählen Sie auf der Seite **Datenmodell** im Aktivitätsbereich **Modell zu Datenquelle zuordnen**.
5. Wählen Sie auf der Seite **Modell zu Datenquelle zuordnen** die Definition **Gruppe**. Wählen Sie im Aktivitätsbereich **Designer** und suchen Sie dann auf der Seite **Modell-Mapping-Design** im Abschnitt **Datenquellen** die Datenquelle „$GeneralJournalEntry“.

  Die Datenquelle „$GeneralJournalEntry“ ist eine berechnete Datensatzliste, die Daten aus der Tabelle **GeneralJournalEntry** bezieht (dies können Sie an der Formel für „$GeneralJournalEntry“ erkennen).
  
6. Suchen Sie im Bereich **Datenquellen** auf der Seite **Modellzuordnungsdesign** nach **GeneralJournalEntry** und wählen Sie diese Tabelle aus.
7. Wählen Sie im Abschnitt **Datenquellen** die Option **Bearbeiten** und aktivieren Sie dann das Kontrollkästchen **Abfrage anfordern** für die Tabelle **GeneralJournalEntry**. Wählen Sie **OK** aus.

![Aktivieren Sie das Kontrollkästchen „Abfrage“ für die Tabelle „Allgemeine Hauptbucheinträge“.](media/ask-for-query-gl-entries.png)

8. Speichern, schließen und schließen Sie die Konfiguration ab.
9. Deaktivieren Sie den Parameter **Standard für Modellzuordnung** für die übergeordnete Konfiguration, **Datenexportmodell**, falls er markiert war. Wählen Sie Ihre abgeleitete Konfiguration als **Standard für die Modellzuordnung**. 

Mit dieser Änderung sehen Sie beim Ausführen von **Datenexport** periodischen Aufgaben **Einzuschließende Datensätze** auf der Inforegister-Registerkarte im Dialogfeld für den Bericht für die Tabelle **Allgemeine Erfassung**. Wählen Sie **Filter**, um Bedingungen für das Filtern von Hauptbucheinträgen festzulegen.

![Filterbedingungen für den periodischen Datenexport einrichten.](media/filter-setup.png)

Um nach dem Feld **Buchungsebene** in der Tabelle **Allgemeine Erfassungsbuchung** zu filtern, wählen Sie **Buchungsebene** in der Spalte **Feld** und dann die erforderliche Buchungsebene in der Spalte **Kriterien**.
