---
title: Höher gestufte Felder für Schritte in der mobilen Warehouse Management-App konfigurieren
description: In diesem Thema wird beschrieben, wie Sie bestimmte Informationen für jeden Schritt in Aufgabenabläufen für die mobile Warehouse Management Mobile App höher stufen und hervorheben.
author: Mirzaab
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 0ce3fb829d349a35c6c2f29838a2c725f7b61c55
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920322"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Höher gestufte Felder für Schritte in der mobilen Warehouse Management-App konfigurieren

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Die Funktionen, die in diesem Thema beschrieben werden, gelten nur für die neue Warehouse Management Mobile-App. Sie betreffen nicht die alte Lager-App, die jetzt außer Betrieb genommen ist.

In diesem Thema wird beschrieben, wie Sie bestimmte Informationen für jeden Schritt in Aufgabenabläufen für die mobile Warehouse Management Mobile App höher stufen und hervorheben. Diese Fähigkeit kann dazu beitragen, die Aufmerksamkeit der Mitarbeiter auf die wichtigsten Bereiche zu lenken, während sie einen Arbeitsfluss durchlaufen. Für jeden Schritt in jedem Prozess können Administratoren auswählen, welche Felder hochgestuft und welche Felder hervorgehoben werden sollen.

## <a name="enable-promoted-fields-in-your-system"></a>Aktivieren Sie heraufgestufte Felder in Ihrem System

Bevor Sie heraufgestufte Felder einrichten können, müssen Sie das folgende Verfahren ausführen, um die erforderlichen Funktionen zu aktivieren und die erforderlichen Feldnamen in der Mobile-App Warehouse Management zu generieren.

1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Funktionsverwaltung**.
1. Aktivieren Sie im [**Funktionsverwaltung**-Arbeitsbereich](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) die Funktion, die wie folgt aufgeführt ist:

    - **Module:** *Lagerortverwaltung*
    - **Name der Funktion:** *Schrittanweisungen für die App "Lager"*

    Für weitere Informationen über die Funktion *Schrittanleitung für die Warehouse-App* siehe [Passen Sie Schritttitel und Anweisungen für die mobile Warehouse Management-App an](mobile-app-titles-instructions.md). Diese Funktion ist Voraussetzung für die Funktion *Heraufgestufte Felder für die Lagerverwaltungs-App*.

1. Aktivieren Sie die Funktion, die folgendermaßen aufgelistet ist:

    - **Module:** *Lagerortverwaltung*
    - **Funktionsname:** *Beworbene Felder für die Lager-App*

    Diese Funktion wird in diesem Thema beschrieben.

1. Aktualisieren Sie die Feldnamen in der mobilen Warehouse Management-App, indem Sie zu **Lagerverwaltung \> Einstellungen \> Mobiles Gerät \> Feldnamen der Warehouse-App** und wählen Sie **Standard-Setup erstellen**. Weitere Informationen finden Sie unter [Felder für die Warehouse Management Mobile App konfigurieren](configure-app-field-names-priorities-warehouse.md).
1. Wiederholen Sie den vorherigen Schritt für jede juristische Person (Firma), in der Sie die mobile App Warehouse Management verwenden.

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Konfigurieren Sie heraufgestufte Felder von einer menüspezifischen Außerkraftsetzung

Verwenden Sie die folgende Prozedur, um heraufgestufte Felder einzurichten.

1. Erstellen Sie eine menüspezifische Überschreibung für das entsprechende Menü und den entsprechenden Schritt wie in [Schritttitel und Anweisungen für die mobile Warehouse Management-App anpassen](mobile-app-titles-instructions.md) beschrieben.
1. Suchen Sie die Kombination der Werte **Schritt-ID** und **Name des Elements**, die Sie bearbeiten wollen, und wählen Sie dann den Wert in der Spalte **Schritt-ID**.
1. Wählen Sie auf der angezeigten Seite im Inforegister **Beworbene Felder auswählen** die Option **Felder auswählen** auf der Symbolleiste.
1. Wählen Sie im Dialogfeld **Heraufgestufte Felder** die Felder aus, die Sie heraufstufen möchten. Sie können auch bis zu zwei der ausgewählten Felder markieren. Hervorgehobene Felder werden in der mobilen Warehouse Management-App fett angezeigt. Bedenken Sie bei der Auswahl von Feldern, dass einige Bildschirme möglicherweise groß genug sind, um nur die oberen ein oder zwei hochgestuften Felder anzuzeigen. Ein Beispiel für die Verwendung dieser Einstellungen finden Sie in dem Szenario weiter unten in diesem Thema.

    > [!NOTE]
    > Die Liste **Verfügbare Felder** ist auf die Felder beschränkt, die für den Menüpunkt erscheinen können. Andere Faktoren (z. B. die Artikelzusammensetzung) bestimmen jedoch, ob ein Feld tatsächlich in der mobilen Warehouse Management-App angezeigt wird. Wenn Sie heraufgestufte Felder konfiguriert haben, werden nur die ausgewählten Felder auf der Hauptseite der mobilen Warehouse Management-App angezeigt. Mitarbeiter können jedoch weiterhin die verbleibenden Felder anzeigen, indem sie auf die Detailseite tippen.

1. Wählen Sie **OK**, um Ihre Einstellungen zu übernehmen. Ihre ausgewählten Felder werden nun im Inforegister **Heraufgestufte Felder auswählen** aufgeführt.

## <a name="example-scenario"></a>Beispielszenario

### <a name="enable-sample-data"></a>Beispieldaten aktivieren

Um die festgelegten Beispieldatensätze und -werte zur Bearbeitung dieses Szenarios zu verwenden, müssen Sie ein System verwenden, auf dem die standardmäßigen Demodaten installiert sind. Sie müssen auch die **USMF** juristische Person auswählen, bevor Sie beginnen.

### <a name="configure-sales-picking-with-promoted-steps-on-the-license-plate-step"></a>Konfigurieren Sie die Verkaufskommissionierung mit beworbenen Schritten auf dem Nummernschildschritt

In diesem Verfahren richten Sie heraufgestufte und hervorgehobene Felder für den Menüpunkt **Verkaufskommissionierung** im Nummernschildschritt ein.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> Mobiles Gerät \> Mobiles Gerät Schritte**.
1. Suchen und wählen Sie die benannte Schritt-ID *LicensePlateId*.
1. Wählen Sie im Aktionsbereich **Schrittkonfiguration hinzufügen**.
1. Verwenden Sie im Dropdown-Dialogfeld das Feld **Menüpunkt** zum Suchen und Auswählen von *Verkaufsauswahl*.
1. Wählen Sie **OK** aus.
1. Die Detailseite für die soeben erstellte Überschreibung wird angezeigt. Wählen Sie auf der Seite im Inforegister **Beworbene Felder auswählen** die Option **Felder auswählen** auf der Symbolleiste.
1. Im Dialogfeld **Heraufgestufte Felder** können Sie die Felder auswählen, die Sie heraufstufen und hervorheben möchten. Suchen und wählen Sie in der Liste **Verfügbare Felder** die folgenden Felder aus und verwenden Sie die Schaltflächen, um sie in die Liste **Ausgewählte Felder** zu verschieben:

    - Elektronische Adresse
    - Artikel
    - Produktname
    - Bestandsstatus

1. Verwenden Sie die Pfeiltasten nach oben und nach unten, um die Reihenfolge der Felder in der Liste **Ausgewählte Felder** anzupassen. In der mobilen Warehouse Management-App werden die Felder in der hier festgelegten Reihenfolge angezeigt.
1. Wählen Sie das Feld **Standort** und wählen Sie dann **Markieren**.
1. Wählen Sie **OK**, um die Konfiguration zu speichern.

### <a name="view-the-promoted-fields-in-the-warehouse-management-mobile-app"></a>Höher gestufte Felder in der mobilen Warehouse Management-App anzeigen

In diesem Verfahren öffnen Sie die mobile Warehouse Management-App und führen die Schritte durch, um die Felder anzuzeigen, die Sie im vorherigen Verfahren heraufgestuft und hervorgehoben haben.

1. Bei Microsoft Dynamics 365 Supply Chain Management erstellen Sie einen Kundenauftrag, der einen Entnahmeschritt erfordert, um von einem Lagerort zu kommissionieren, für den ein Nummernschild verfolgt wird. Dann geben Sie den Auftrag für den Lagerort frei. Notieren Sie sich die erstellte Arbeits-ID.
1. Öffnen Sie die Warehouse Management Mobile App und melden Sie sich bei Lagerort 24 an. (Melden Sie sich bei den Standard-Demo-Daten mit *24* als Benutzer-ID und *1* als Passwort an.)
1. Wählen Sie das Menü **Ausgehend** und wählen Sie dann den Menüpunkt **Verkaufsauswahl**.
1. Befolgen Sie die Anweisungen zur Dateneingabe auf dem Bildschirm, um die in Schritt 1 generierte Arbeits-ID einzugeben.
1. Auf dem Schritt, der den Text **Scannen Sie ein Nummernschild** enthält, sollten Sie die vorgenommenen Änderungen auf der Detailseite sehen. Die Felder werden in der Reihenfolge angezeigt, die Sie für die heraufgestuften Felder festgelegt haben, und das Feld **Standort** ist fett dargestellt.