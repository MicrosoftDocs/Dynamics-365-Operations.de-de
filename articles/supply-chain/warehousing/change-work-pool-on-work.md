---
title: Arbeitspool für Arbeit ändern
description: In diesem Thema wird erläutert, wie Sie die Schaltfläche „Arbeitspool ändern“ für Arbeitsaufgaben verwenden können, um den Arbeitspool vorhandener Arbeit zu ändern.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 61b988cf2501812e940f726e02d8fc1bcee2c035
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233054"
---
# <a name="change-work-pool-on-work"></a>Arbeitspool für Arbeit ändern

[!include [banner](../includes/banner.md)]

Sie können Arbeitspools verwenden, um die Arbeit in Gruppen organisieren. So können Sie beispielsweise einen Arbeitspool erstellen, um Arbeit zu klassifizieren, die an einem bestimmten Lagerort auftritt.

Die Funktion *Arbeitspool bei Arbeit ändern* fügt dem Aktionsbereich für Arbeitsaufgaben eine Schaltfläche **Arbeitspool ändern** hinzu. Daher können Lagerverwalter den Arbeitspool vorhandener Arbeit problemlos ändern. Mit dieser Funktion können Manager schnell auf Änderungen vor Ort im Lager reagieren und sie können sich leichter auf ändernde Situationen anpassen und Arbeit an einen anderen Arbeitspool übertragen.

## <a name="turn-on-the-change-work-pool-on-work-feature"></a>Die Funktion „Arbeitspool bei Arbeit ändern“ aktivieren

Bevor Sie mit der Einrichtung oder Verwendung dieser Funktion beginnen, müssen Sie sicherstellen, dass sie in Ihrem System verfügbar ist. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Arbeitspool bei Arbeit ändern*

## <a name="set-up-the-change-work-pool-on-work-feature"></a>Die Funktion „Arbeitspool bei Arbeit ändern“ einrichten

Um diese Funktion nutzen zu können, müssen einige Arbeitspools eingerichtet sein. Sie können Ihre Arbeitsvorlagen auch so einrichten, dass sie automatisch einen Pool zuweisen. Wenn Sie das weiter unten in diesem Thema enthaltene Beispielszenario durcharbeiten möchten, richten Sie Ihr System wie in diesem Abschnitt beschrieben ein.

### <a name="set-up-work-pools"></a>Arbeitspools einrichten

Mit Arbeitspools können Sie Arbeitsaufgaben nach Typ organisieren. Um mit der Funktion *Arbeitspool bei Arbeit ändern* zu arbeiten, müssen mindestens zwei Arbeitspools verfügbar sein. Gehen Sie folgendermaßen vor, um Arbeitspools anzuzeigen und hinzuzufügen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitspools**.
1. Wenn Sie mit Demodaten aus dem Unternehmen **USMF** arbeiten und das Beispielszenario später in diesem Thema durcharbeiten werden, fügen Sie zwei Arbeitspools mit den folgenden Einstellungen hinzu:

    - Arbeitspool 1:

        - **Arbeitspool-ID:** *Webshop*
        - **Beschreibung:** *Webshop*

    - Arbeitspool 2:

        - **Arbeitspool-ID:** *CallCenter*
        - **Beschreibung:** *Callcenter*

1. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="set-up-work-templates"></a>Arbeitsvorlagen einrichten

Für jede Ihrer Arbeitsvorlagen können Sie nach Bedarf einen Standardarbeitspool festlegen. Für jede relevante Vorlage weisen Sie in der Spalte **Arbeitspool-ID** einen Arbeitspool hinzu. In diesem Fall erben alle Arbeitsaufgaben, die mithilfe einer bestimmten Vorlage generiert werden, automatisch den zugewiesenen Arbeitspool. Wenn Sie mit Demodaten aus dem Unternehmen **USMF** arbeiten und das Beispielszenario später in diesem Thema durcharbeiten werden, folgen Sie diesen Schritten.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Klicken Sie im Aktionsbereich auf **Bearbeiten**, um die Seite in den Bearbeitungsmodus zu versetzen.
1. Bearbeiten Sie die Vorlage, indem Sie die folgenden Werte festlegen:

    - **Arbeitsvorlage:** *62 entnehmen für Paket*
    - **Arbeitspool-ID:** *Webshop*

1. Wählen Sie **Speichern** aus.

## <a name="example-scenario"></a>Beispielszenario

Dieses Szenario zeigt, wie Sie den Stream der Verarbeitung für eine vorhandene Arbeitsaufgabe ändern, indem Sie dessen Arbeitspool ändern. Es verwendet Demodaten aus dem Unternehmen **USMF** und die Einstellungen, die zuvor in diesem Thema vorgeschlagen wurden.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Einen Auftrag erstellen und ihn für den Lagerort freigeben

1. Bestätigen Sie, dass genügend verfügbarer Lagerbestand für Artikel *A0001* und *A0002* im Lagerort *62* vorhanden ist. Gehen Sie zu **Lagerverwaltung \> Anfragen und Berichte \> Bestandsliste** und bearbeiten Sie die Filter wie hier gezeigt:

    - Der Wert **Lagerort** beginnt mit *62*.
    - Der Wert **Artikelnummer** ist entweder *A001* oder *A002*.

    Demodaten sollten jeweils eine Menge von 10 haben.

    Als nächstes müssen Sie einen Auftrag erstellen.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-007*
    - **Lagerort:** *62*

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.
1. Der neue Auftrag wird geöffnet. Es sollte eine neue, leere Position im Raster auf dem Inforegister **Auftragspositionen** enthalten. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikelnummer** *A001*
    - **Menge** *2*

1. Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, um den Lagerbestand zu reservieren.
1. Schließen Sie die Seite.
1. Wählen Sie im Inforegister **Auftragspositionen** die Option **Position hinzufügen** aus, um Ihrem Auftrag eine weitere Position hinzuzufügen. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikelnummer:** *A0002*
    - **Menge** *2*

1. Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, um den Lagerbestand zu reservieren.
1. Schließen Sie die Seite.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.
1. Sie erhalten Informationsnachrichten mit der Wellen-ID und der Lieferungs-ID, die von der Freigabe erstellt wurden. Notieren Sie die Wellen-ID.

### <a name="review-the-outbound-wave"></a>Die ausgehende Welle überprüfen

1. Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.
1. Suchen Sie im Raster nach der Wellen-ID, die von der Freigabe des Auftrags erstellt wurde.
1. Wählen Sie die Wellen-ID aus, um die Details anzuzeigen.
1. Im Inforegister **Wellenpositionen** stellen Sie sicher, dass eine Lieferungs-ID für den Auftrag angezeigt wird.

    > [!TIP]
    > Wenn die Option **Welle bei Freigabe für Lagerort verarbeiten** auf *Nein* in den Einstellungen für die Lieferungswellenvorlage festgelegt ist, müssen Sie die Welle manuell verarbeiten, indem Sie **Verarbeiten** aus der Registerkarte **Welle** im Aktionsbereich auswählen, um Arbeit zu erstellen.

1. Stellen Sie sicher, dass die Welle verarbeitet wurde. Diese Verarbeitung erstellt die erforderliche Arbeit.

### <a name="view-work-details-and-change-the-work-pool"></a>Arbeitsdetails anzeigen und den Arbeitspool ändern

Sie können die Seite **Arbeitsdetails** verwenden, um die erstellte Arbeit anzuzeigen und den Arbeitspool zu verwalten.

1. Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.
1. Wählen Sie die Zeile für die gerade erstellte Arbeit aus. Die Spalte **Auftragsnummer** zeigt die Auftragsnummer an.

    Das Feld **Arbeitspool-ID** wird auf die Arbeitspool-ID festgelegt, die in der Arbeitsvorlage eingerichtet wurde.

    > [!TIP]
    > Wenn Sie das Feld **Arbeitspool-ID** nicht sehen, fügen Sie die Spalte zum Raster hinzu und aktualisieren Sie die Seite.

1. Um den Arbeitspool zu ändern, der der Arbeits-ID zugeordnet ist, wählen Sie im Aktionsbereich auf der Registerkarte **Arbeit** die Option **Arbeitspool-ID** ändern aus.
1. Im Dialogfeld **Arbeitspool ändern** im Inforegister **Parameter** im Feld **Arbeitspool-ID** wählen Sie *Callcenter* aus.
1. Wählen Sie **OK**, um Ihre Änderung zu übernehmen.
1. Beachten Sie, dass der Wert des Felds **Arbeitspool-ID** jetzt zu *Callcenter* geändert wurde.

> [!IMPORTANT]
> Wenn das Dialogfeld **Arbeitspool ändern** angezeigt wird, ist das Feld **Arbeitspool-ID** möglicherweise standardmäßig leer. Wenn das Feld leer ist, wenn Sie **OK** auswählen, um Änderungen zu übernehmen, entfernen Sie den Arbeitspool vollständig aus der Arbeit.
>
> Zusätzlich zum Wechseln des Arbeitspools können Sie mit dieser Prozedur jeder Arbeitsaufgabe, die keinen hat, einen Arbeitspool hinzufügen oder einen Arbeitspool aus jeder Arbeitsaufgabe entfernen, die einen hat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]