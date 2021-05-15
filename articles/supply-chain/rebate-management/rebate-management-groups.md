---
title: Rückvergütungsverwaltungsgruppen
description: In diesem Thema wird beschrieben, wie Sie Rückvergütungsverwaltungsgruppen festlegen. Rückvergütungsverwaltungsgruppen können bei Rückvergütungsberechnungen verwendet und an einen Masterdatensatz angehängt werden.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: cef7abbbf2a94e26b6b9e66492cd7347d3b4d1f2
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920060"
---
# <a name="rebate-management-groups"></a>Rückvergütungsverwaltungsgruppen

[!include [banner](../includes/banner.md)]

Rückvergütungs- und Abzugsberechnungen können von Gruppen gesteuert werden. Rückvergütungsverwaltungsgruppen können für Debitoren, Kreditoren und Artikel erstellt werden. Sie können an einen Masterdatensatz angehängt werden.

## <a name="rebate-management-customer-groups"></a>Rückvergütungsverwaltungs-Debitorengruppen

Die Berechnung für eine Debitorengruppe wird häufig für eine Unternehmenskette erstellt, z. B. eine Supermarktkette oder ein Franchise-Unternehmen. Dieser Berechnungstyp bezieht sich normalerweise auf eine Rückvergütung.

Ein Abzug wird häufig berechnet, ohne zu berücksichtigen, an wen der qualifizierende Auftrag verkauft wurde. Es gibt jedoch auch Ausnahmen. Beispielsweise kann ein Lizenznehmer ein Abzugssystem erstellen, bei dem Debitorengruppe A 4 % erhält, Debitorengruppe B jedoch nur 3 %.

### <a name="set-up-customer-groups"></a>Debitorengruppen einrichten

Um in der Rückvergütungsverwaltung mit Debitorengruppen zu arbeiten, gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsgruppen einrichten \> Debitorengruppen**. Sie können die Schaltflächen im Aktivitätsbereich verwenden, um Gruppen bei Bedarf hinzuzufügen und zu entfernen. Legen Sie für jede Gruppe die folgenden Felder fest:

- **Rückvergütungsverwaltungsgruppe** – Geben Sie der Gruppe einen einzigartigen Namen.
- **Beschreibung** – Geben Sie eine Beschreibung der Gruppe ein, um weitere Informationen zur Verwendung bereitzustellen.

### <a name="manage-customer-group-assignments"></a>Debitorengruppenzuweisungen verwalten

Jeder Debitor kann einer beliebigen Anzahl von Rückvergütungsverwaltungsgruppen angehören. Um Gruppenmitglieder anzuzeigen und zuzuweisen, können Sie entweder von der Gruppen- oder der Debitorenliste ausgehen.

Gehen Sie wie folgt vor, um Debitoren einer ausgewählten Gruppe anzuzeigen, dazu hinzuzufügen oder daraus zu entfernen.

1. Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsgruppen einrichten \> Debitorengruppen**.
1. Wählen Sie die zu verwaltende Gruppe aus.
1. Wählen Sie im Aktivitätsbereich **Debitoren** aus. Die Seite **Rückvergütungsverwaltungsgruppen** wird angezeigt und zeigt eine Liste der Debitoren an, die bereits Mitglieder der ausgewählten Gruppe sind.
1. Um einer Gruppe einen neuen Debitor hinzuzufügen, wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster eine neue Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Debitorenkonto** – Wählen Sie die ID des Debitorenkontos aus.
    - **Name** – Geben Sie einen Namen und/oder eine Beschreibung des Debitors ein.

1. Um einen Debitor aus der Gruppe zu entfernen, wählen Sie ihn aus und wählen Sie dann im Aktivitätsbereich **Löschen** aus.

Gehen Sie wie folgt vor, um Gruppenzuweisungen für einen ausgewählten Debitor anzuzeigen, hinzuzufügen oder entfernen.

1. Gehen Sie zu **Debitorenkonten \> Debitoren \> Alle Debitoren**.
1. Wählen Sie den Debitor aus, mit dem Sie arbeiten möchten.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Debitor** in der Gruppe **Rückvergütungsverwaltung** die Option **Rückvergütungsverwaltungsgruppen** aus. Die Seite **Rückvergütungsverwaltungsgruppen** wird angezeigt und zeigt eine Liste der Gruppen an, zu denen der ausgewählte Debitor bereits gehört.
1. Um den Debitor einer neuen Gruppe hinzuzufügen, wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster eine neue Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Rückvergütungsverwaltungsgruppen** – Wählen Sie die Gruppe aus, zu der der Debitor hinzugefügt werden soll.
    - **Beschreibung** – Geben Sie eine Beschreibung der Gruppe ein (um beispielsweise zu erklären, warum der Debitor Mitglied der Gruppe ist).

1. Um einen Debitor aus einer Gruppe zu entfernen, wählen Sie die Gruppe aus und wählen Sie dann im Aktivitätsbereich **Löschen** aus.

## <a name="rebate-management-vendor-groups"></a>Rückvergütungsverwaltungs-Kreditorengruppen

Die Berechnung für eine Gruppe von Kreditoren wird häufig für eine Gruppe von Zustellungsorten erstellt. Dieser Berechnungstyp bezieht sich normalerweise auf eine Rückvergütung.

### <a name="set-up-vendor-groups"></a>Kreditorengruppen einrichten

Um in der Rückvergütungsverwaltung mit Kreditorengruppen zu arbeiten, gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsgruppen einrichten \> Kreditorengruppen**. Sie können die Schaltflächen im Aktivitätsbereich verwenden, um Gruppen bei Bedarf hinzuzufügen und zu entfernen. Legen Sie für jede Gruppe die folgenden Felder fest:

- **Rückvergütungsverwaltungsgruppe** – Geben Sie der Gruppe einen einzigartigen Namen.
- **Beschreibung** – Geben Sie eine Beschreibung der Gruppe ein, um weitere Informationen zur Verwendung bereitzustellen.

### <a name="manage-vendor-group-assignments"></a>Kreditorengruppenzuweisungen verwalten

Jeder Kreditor kann einer beliebigen Anzahl von Rückvergütungsverwaltungsgruppen angehören. Um Gruppenmitglieder anzuzeigen und zuzuweisen, können Sie entweder von der Gruppen- oder der Kreditorenliste ausgehen.

Gehen Sie wie folgt vor, um Kreditoren einer ausgewählten Gruppe anzuzeigen, dazu hinzuzufügen oder daraus zu entfernen.

1. Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsgruppen einrichten \> Kreditorengruppen**.
1. Wählen Sie die zu verwaltende Gruppe aus.
1. Wählen Sie im Aktivitätsbereich **Kreditoren** aus. Die Seite **Rückvergütungsverwaltungsgruppen** wird angezeigt und zeigt eine Liste der Kreditoren an, die bereits Mitglieder der ausgewählten Gruppe sind.
1. Um einer Gruppe einen neuen Kreditor hinzuzufügen, wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster eine neue Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Kreditorenkonto** – Wählen Sie die ID des Kreditorenkontos aus.
    - **Name** – Geben Sie einen Namen und/oder eine Beschreibung des Kreditor ein.

1. Um einen Kreditor aus der Gruppe zu entfernen, wählen Sie ihn aus und wählen Sie dann im Aktivitätsbereich **Löschen** aus.

Gehen Sie wie folgt vor, um Gruppenzuweisungen für einen ausgewählten Kreditor anzuzeigen, hinzuzufügen oder entfernen.

1. Gehen Sie zu **Kreditorenkonten \> Kreditoren \> Alle Kreditoren**.
1. Wählen Sie den Kreditor aus, mit dem Sie arbeiten möchten.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Kreditor** in der Gruppe **Rückvergütungsverwaltung** die Option **Rückvergütungsverwaltungsgruppen** aus. Die Seite **Rückvergütungsverwaltungsgruppen** wird angezeigt und zeigt eine Liste der Gruppen an, zu denen der ausgewählte Kreditor bereits gehört.
1. Um den Kreditor einer neuen Gruppe hinzuzufügen, wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster eine neue Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Rückvergütungsverwaltungsgruppen** – Wählen Sie die Gruppe aus, zu der der Kreditor hinzugefügt werden soll.
    - **Beschreibung** – Geben Sie eine Beschreibung der Gruppe ein (um beispielsweise zu erklären, warum der Kreditor Mitglied der Gruppe ist).

1. Um einen Kreditor aus einer Gruppe zu entfernen, wählen Sie die Gruppe aus und wählen Sie dann im Aktivitätsbereich **Löschen** aus.

## <a name="item-rebate-groups"></a>Artikelrückvergütungsgruppen

Durch die Gruppierung von Artikeln haben Sie mehr Flexibilität bei der Berechnung von Rückvergütungen und Abzügen. Dieser Ansatz ist häufig eine effizientere Methode, um Rückvergütungen und Abzüge für Debitoren und Kreditoren einzurichten.

### <a name="set-up-item-groups"></a>Artikelgruppen einrichten

Um in der Rückvergütungsverwaltung mit Artikelgruppen zu arbeiten, gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsgruppen einrichten \> Artikelgruppen**. Sie können die Schaltflächen im Aktivitätsbereich verwenden, um Gruppen bei Bedarf hinzuzufügen und zu entfernen. Legen Sie für jede Gruppe die folgenden Felder fest:

- **Rückvergütungsverwaltungsgruppe** – Geben Sie der Gruppe einen einzigartigen Namen.
- **Beschreibung** – Geben Sie eine Beschreibung der Gruppe ein, um weitere Informationen zur Verwendung bereitzustellen.

### <a name="manage-item-group-assignments"></a>Artikelgruppenzuweisungen verwalten

Jeder Artikel kann einer beliebigen Anzahl von Rückvergütungsverwaltungsgruppen angehören. Um Gruppenmitglieder anzuzeigen und zuzuweisen, können Sie entweder von der Gruppen- oder der Artikelliste ausgehen. Sie können Artikel auch basierend auf Ihrer Kategoriehierarchie hinzufügen.

Gehen Sie wie folgt vor, um Artikel einer ausgewählten Gruppe anzuzeigen, dazu hinzuzufügen oder daraus zu entfernen.

1. Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsgruppen einrichten \> Artikelgruppen**.
1. Wählen Sie die zu verwaltende Gruppe aus.
1. Klicken Sie im Aktivitätsbereich auf **Artikel**. Die Seite **Rückvergütungsverwaltungsgruppen** wird angezeigt und zeigt eine Liste der Artikel an, die bereits zur ausgewählten Gruppe gehören.
1. Um einer Gruppe einen neuen Artikel hinzuzufügen, wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster eine neue Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Artikelkonto** – Wählen Sie die ID des Artikelkontos aus.
    - **Produktname** – Geben Sie einen Namen und/oder eine Beschreibung des Artikels ein.

1. Um einen Artikel aus der Gruppe zu entfernen, wählen Sie ihn aus und wählen Sie dann im Aktivitätsbereich **Löschen** aus.

Gehen Sie wie folgt vor, um Gruppenzuweisungen für einen ausgewählten Artikel anzuzeigen, hinzuzufügen oder entfernen.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie den Artikel aus, mit dem Sie arbeiten möchten.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Rückvergütungsverwaltung** die Option **Rückvergütungsverwaltungsgruppen** aus. Die Seite **Rückvergütungsverwaltungsgruppen** wird angezeigt und zeigt eine Liste der Gruppen an, zu denen der ausgewählte Artikel bereits gehört.
1. Um den Artikel einer neuen Gruppe hinzuzufügen, wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster eine neue Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Rückvergütungsverwaltungsgruppen** – Wählen Sie die Gruppe aus, zu der der Artikel hinzugefügt werden soll.
    - **Beschreibung** – Geben Sie eine Beschreibung der Gruppe ein (um beispielsweise zu erklären, warum der Artikel Mitglied der Gruppe ist).

1. Um einen Artikel aus einer Gruppe zu entfernen, wählen Sie die Gruppe aus und wählen Sie dann im Aktivitätsbereich **Löschen** aus.

Führen Sie die folgenden Schritte aus, um einer Gruppe basierend auf Ihrer Kategoriehierarchie Artikel hinzuzufügen.

1. Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsgruppen einrichten \> Artikelgruppen**.
1. Wählen Sie die zu verwaltende Gruppe aus.
1. Klicken Sie im Aktivitätsbereich auf **Artikel hinzufügen**.
1. Wählen Sie im Feld **Kategoriehierarchie** im Dialogfeld **Artikel hinzufügen** eine Kategorie der obersten Ebene aus.
1. Die Artikelhierarchie wird im linken Bereich geöffnet. Wählen Sie die Hierarchieebene aus, nach der Sie suchen. 
1. Artikel der ausgewählten Hierarchie und Hierarchieebene werden jetzt im rechten Bereich aufgelistet. Führen Sie die folgenden Schritte aus, um mit dem Bereich zu arbeiten:

    - Aktivieren Sie für alle hinzuzufügenden Artikel das entsprechende Kontrollkästchen.
    - Aktivieren Sie das Kontrollkästchen in der Rasterkopfzeile, um alle aufgelisteten Artikel auszuwählen.
    - Wählen Sie die Schaltfläche **Ausgewählte anzeigen**, um das Raster so zu filtern, dass nur die Artikel angezeigt werden, die Sie bisher ausgewählt haben. Klicken Sie erneut auf die Schaltfläche, um zur vollständigen Liste zurückzukehren.

1. Wählen Sie **OK**, um Ihre Artikelauswahl auf die ausgewählte Gruppe anzuwenden.
