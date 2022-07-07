---
title: BestellungErstellen von Anlagen basierend auf den Bestellungen
description: In diesem Artikel wird erläutert, wie Sie eine Liste von Anlageposten erstellen können, die als Grundlage für die Erstellung von Anlagen für Wartungsaufträge im Asset-Management verwendet werden können.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccd14493aac6484dc54ccf51ae159a071c8697a5
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015608"
---
# <a name="create-assets-based-on-purchase-orders"></a>BestellungErstellen von Anlagen basierend auf den Bestellungen

[!include [banner](../../includes/banner.md)]

 

In diesem Artikel wird erläutert, wie Sie eine Liste von Anlageposten erstellen können, die als Grundlage für die Erstellung von Anlagen für Wartungsaufträge im Asset-Management verwendet werden können. Basierend auf Anlageartikeln können Sie eine Liste der Bestellungen anzeigen, die für diesen Artikel erstellt wurden. Der Zweck dieser Funktion ist es, einfach eine Anlage im Asset-Management basierend auf einer Bestellung zu erstellen.

Zuerst richten Sie Artikel ein, die für das Erstellen von Anlagen für eine Bestellung in **Anlageartikel** verwendet werden kann. Nachdem Sie einer Bestellposition erstellt haben, erstellen Sie die Anlage unter **Pendente Anlagen**. Es ist möglihc zu entscheid, in welcher Phase der Bestellung die Anlage erstellt werden sollte.


## <a name="select-asset-items"></a>Anlageartikel auswählen

1. Klicken Sie auf **Anlagt-Management** > **Einstellungen** > **Anlagen** > **Artikel**.
2. Klicken Sie auf **Neu**, um einen neuen Anlageartikel zu erstellen.
3. Wählen Sie im Feld **Artikelnummer** einen Artikel aus. Wenn Sie dieses Feld leer lassen, wird der Name automatisch im Feld **Produktname** eingefügt.
4. Auf dem Inforegister **Allgemeines** wählen Sie einen Anlagentyp für den Artikel aus.
5. Wählen Sie Anlagenhersteller und -Modell für den Artikel aus.
6. Speichert den Artikel.


## <a name="create-assets-from-pending-assets"></a>Anlagen erstellen aus den ausstehenden Anlagen

1. Klicken Sie auf **Anlagenmanagement** > **Anlagen** > **Ausstehende Anlagen**.
2. Sie finden eine aktualisierte Liste der Bestellungen auf der Grundlage der Artikel, die unter **Anlageartikel** ausgewählt werden.
3. Sie können den Status von Bestellungen filtern, um auszuwählen, in welchem Lebenszyklusstatus die Anlage erstellt werden soll. Beispielsweise sollten Sie nur Anlagen erstellen, wenn ein Produktzugang für eine Bestellung gebucht wurde.
4. Wählen Sie den Link **Referenznummer** auf einer Bestellposition aus, um die detaillierte Informationen zum Artikel anzuzeigen.
5. Wenn Sie bearbeiten möchten, welche Dimensionen auf dem Inforegister **Bestanddimensionen** angezeigt werden, klicken Sie auf die Schaltfläche **Anzeigen-Dimensionen**, und treffen Sie Ihre Auswahl.
6. Wenn Sie eine Anlage basierend  auf einer Bestellposition erstellen möchten, aktivieren Sie das Kontrollkästchen in der Spalte **Markieren** für diese Position auf der Listenseite aus, und klicken Sie **Anlagen erstellen**. Eine Meldung wird angezeigt, die Sie über die Anlage-Kennung informiert.
7. Wählen Sie die Anlage in der Liste **Alle Anlagen** aus und klicken **Bearbeiten**, um weitere Informationen zur Anlage hinzuzufügen.
8. Unter **Ausstehende Anlagen** wenn Sie eine Position löschen möchten, da Sie keine Anlage erstellen möchten, wählen Sie das Kontrollkästchen in der Spalte **Markieren** für diese Position und klicken Sie **Ausstehende Anlage ignorieren**. Eine Meldung wird angezeigt, die Sie über die Anlage-Kennung informiert. Löschen Sie nicht die Bestellung bzw. den Auftrag, nur den Datensatz, von dem Sie die Anlage in **Anlage-Management** erstellt haben könnten.

>[!NOTE]
>Alle Produktdimensionen (Größe, Farbe, Konfigurationsusw.) werden automatisch in die Anlagenattribute übertragen. Rückverfolgungsdimensionen (Seriennummer) werden direkt für die Anlage aufbewahrt, wenn die Anlage erstellt wird.


## <a name="find-pending-assets"></a>Suchen Sie ausstehende Anlagen

Sie können **Ausstehende Anlagenanzahl** ausführen, um ausstehende Anlagen zu prüfen. Beispielsweise kann diese Funktion zum Empfangen einer Benachrichtigung verwendet werden, wenn eine der Anlage fertig ist, als Anlage erstellt zu werden.

1. Klicken Sie auf **Anlage-Management** > **Gemeinsam** > **Anlagen** > **Ausstehende Anlagenzählung**.
2. Klicken Sie **OK**, um den Einzelvorgang zu aktivieren und die Liste in **Ausstehende Anlagen** zu aktualisieren.
3. Sie können diesen Einzelvorgang als Batchauftrag einrichten, so dass er beispielsweise einmal pro Tag ausgeführt wird.

**Vorsicht:**, Wenn Daten in einer Bestellung geändert werden, *nachdem* Sie eine Anlage auf Basis des dazu gehörenden Artikels erstellt haben, werden diese Änderungen nicht in der Anlage angezeigt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]