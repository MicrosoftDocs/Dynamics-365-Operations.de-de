---
title: Bearbeitung von internen Daten in Hauptbuchbelegen zulassen
description: Dieser Artikel enthält Informationen zum Bearbeiten interner Daten auf Hauptbuchbelegen.
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 26fc6518f0b4eae815e047db1dbaadd7c56a2e67
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220664"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>Bearbeitung von internen Daten in Hauptbuchbelegen zulassen

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]


Wenn Sie Buchhaltungseinträge in das Hauptbuch buchen, wird häufig das Feld **Beschreibung** verwendet, um interne Notizen oder Dokumentationen zu speichern. Falsche Angaben können Verwirrung stiften und den Periodenabschluss erschweren. Mit dieser Funktion kann der Buchhaltungsmanager oder der Supervisor Buchhaltung Fehler beheben, indem er das Feld **Beschreibung** auf gebuchten Belegen im Hauptbuch bearbeitet.

Änderungen an gebuchten Belegen im Hauptbuch beschränken sich auf Daten interner Natur. Mit dieser Funktion können Sie niemals Daten wie Beträge, Buchungsdaten, Sachkonten und die Buchungswährung bearbeiten. Änderungen an diesen Daten wirken sich auf die externe Finanzaufstellung aus und dürfen nur über neue Hauptbuchbelege erfolgen.

> [!NOTE]
> Bei Dynamics 365 Finance der Version 10.0.29 ist diese Funktion auf Bearbeitungen des Felds **Beschreibung** beschränkt.

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>Internen Daten in Hauptbuchbelegen bearbeiten

Bevor interne Daten zu Hauptbuchbelegen bearbeitet werden können, müssen Sie die Funktion **Bearbeitung von internen Daten in Hauptbuchbelegen zulassen** im Arbeitsbereich **Funktionsverwaltung** aktivieren.
Nachdem die Funktion aktiviert wurde, muss dem Benutzer, der gebuchte Belege bearbeiten wird, die Rolle „Buchhaltungsmanager“ oder „Supervisor Buchhaltung“ zugewiesen werden. Sie können auch anderen Rollen Berechtigungen erteilen, indem Sie die Sicherheitsrollen anpassen.

Der Bearbeitungsprozess ist nur auf der Seite „Belegbuchungen“ zulässig.

1. Wechseln Sie zu **Hauptbuch** > **Abfragen und Berichte** > **Belegbuchungen**.
2. Geben Sie im Dialogfeld **SysQuery** Suchkriterien ein, um Belege auszuwählen.
3. Wählen Sie die Positionen für die Belege aus, die Sie bearbeiten möchten, und wählen Sie dann **Beleg bearbeiten** > **Interne Belegdaten bearbeiten** aus.

    [![Seite „Belegbuchungen“.](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
Auf der Seite **Interne Belegdaten bearbeiten** werden die folgenden Daten für jede Position angezeigt, die Sie ausgewählt haben:
  
  - Sachkonto
  - Kontoname
  - Beleg
  - Aktuelle Beschreibung
  - Neue Beschreibung

    [![Alle Journale.](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> Nur das Feld **Neue Beschreibung** kann bearbeitet werden. Standardmäßig stimmt der Wert mit dem Wert des Felds **Aktuelle Beschreibung** überein, damit Sie kleinere Fehler in der Beschreibung schnell beheben können.

4. Ändern Sie das Feld **Neue Beschreibung** in jeder Position oder löschen Sie die Beschreibung aus jeder Position.

   Wenn mehrere Positionen mit demselben Wert aktualisiert werden müssen, gehen Sie alternativ wie folgt vor:

      1. Wählen Sie die zu bearbeitenden Positionen und dann **Sammelaktualisierung ausgewählter Datensätze** aus.
      2. Wählen Sie im Feld **Zu bearbeitendes Feld** das zu bearbeitende Feld aus. Derzeit enthält die Suche nur das Feld **Neue Beschreibung**.
      3. Geben Sie im Feld **Neuer Wert** eine neue Beschreibung ein.
      4. Wählen Sie **Aktualisieren**. Alle ausgewählten Datensätze werden mit dem neuen Wert aktualisiert.

      [![Dialogfeld „Sammelaktualisierung ausgewählter Datensätze“.](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. Geben Sie im Feld **Grund für Bearbeitung** eine Anmerkung ein, um zu erklären, warum die Änderung vorgenommen wurde. Diese Notiz wird auf der Seite **Überwachungspfad für Belegbearbeitungen** angezeigt.

   An demselben Beleg können mehrere Änderungen vorgenommen werden. Jede Änderung wird nachverfolgt.

## <a name="audit-trail-of-voucher-edits"></a>Audit-Trail der Belegbearbeitungen

Ein Überwachungspfad wird speziell gepflegt, um die Änderungen zu verfolgen, die durch diese Funktion vorgenommen werden. Sie können auf zwei Arten auf den Überwachungspfad von Belegbearbeitungen zugreifen:

  - Wechseln Sie zu **Hauptbuch** > **Abfragen und Berichte** > **Belegbuchungen**. Wählen Sie auf der Seite **Belegabfragen** **Beleg bearbeiten** > **Überwachungspfad von Belegbearbeitungen**. Der Überwachungspfad wird nur für den ausgewählten Belegdatensatz angezeigt. 
   
    Wenn Sie die Anfrage auf diese Weise öffnen, können Sie sich auf alle Änderungen konzentrieren, die an einem einzelnen Belegdatensatz vorgenommen wurden.
  
  - Gehen Sie zu **Hauptbuch** > **Periodische Aufgaben** > **Überwachungspfad von Belegbearbeitungen**. Geben Sie im Dialogfeld Kriterien ein, um anzugeben, für welche Belege der Überwachungspfad der Bearbeitungen angezeigt werden soll. Um den Überwachungspfad für alle Belege anzuzeigen, lassen Sie die Kriterien leer und wählen Sie **OK** aus. 
    
    Indem Sie die Abfrage auf diese Weise öffnen, können Sie nach Änderungen filtern, die an einem bestimmten Datum oder von einem bestimmten Benutzer vorgenommen wurden.

Die Seite **Überwachungspfad der Bearbeitungen** zeigt die folgenden Informationen:

- **Datum und Uhrzeit der Erstellung**: Datum und Uhrzeit der Bearbeitung.
- **Grund für Bearbeitung**: Der Grund, den der Benutzer für die Bearbeitung eingegeben hat.
- **Erstellt von**: Der Benutzer, der die Bearbeitung vorgenommen hat.

Um die Details der einzelnen Überwachungspfade anzuzeigen, führen Sie einen Drilldown auf den Wert **Datum und Uhrzeit der Erstellung** aus. Die Seite **Bearbeitete Belegeigenschaften anzeigen** zeigt dieselben Informationen wie die ursprüngliche Bearbeitungsseite, einschließlich der vorherigen und der aktualisierten Beschreibung.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
