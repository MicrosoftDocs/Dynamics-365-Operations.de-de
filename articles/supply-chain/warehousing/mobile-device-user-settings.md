---
title: Benutzereinstellungen für das mobile Gerät
description: Dieser Artikel erklärt, wie Sie die Benutzereinstellungen für mobile Geräte für Arbeitskräfte im Lagerort verwalten.
author: Mirzaab
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppDeviceBrand,WHSMobileAppUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 15f9ce1768e1ed9dc6f7e84d245082b46a7f122c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882343"
---
# <a name="mobile-device-user-settings"></a>Benutzereinstellungen für das mobile Gerät

[!include [banner](../../includes/banner.md)]

Die neue mobile App Lagerortverwaltung verfügt über eine Reihe von App-spezifischen Einstellungen, die helfen, die Benutzererfahrung anzupassen. Da die App auf Geräten mit unterschiedlichen Bildschirmgrößen und Konfigurationen (z. B. Tablet, Telefon oder Arm-held) verwendet werden kann, kann es sinnvoll sein, diese Einstellungen zentral von Microsoft Dynamics 365 Supply Chain Management aus zu verwalten.

Mit der Funktion *Benutzereinstellungen für mobile Geräte* können Sie globale Benutzereinstellungen festlegen, die auf allen Geräten verwendet werden. Sie können auch granularere Benutzereinstellungen für einzelne Marken, Gerätemodelle und/oder Arbeitskräfte festlegen. Wenn sich eine Arbeitskraft in der mobilen App der Lagerortverwaltung anmeldet, holt die App das spezifischste Einstellungsprofil, das in der Supply Chain Management für die entsprechende Marke, das Gerät und/oder die Benutzer-ID gespeichert ist, und wendet es an.

Diese Funktion kann Arbeitskräften helfen, schneller loszulegen, wenn sie beginnen, ein neues Gerät zu verwenden. Im Folgenden finden Sie einige Beispiele hierfür:

- Admins können einen Standard-Satz von Einstellungen festlegen, die am besten für Geräte eines bestimmten Herstellers und/oder für bestimmte Gerätemodelle funktionieren. So können Arbeitskräfte mit einem neuen Gerät loslegen, ohne unbedingt die Einstellungen ändern zu müssen.
- Wenn Ihre Firma über einen Pool identischer Geräte verfügt, die von den Arbeitskräften gemeinsam genutzt werden, sehen die Arbeitskräfte ihre bevorzugte Einrichtung jedes Mal, wenn sie sich anmelden, auch wenn sie das spezifische physische Gerät, das sie an einem bestimmten Tag ausgewählt haben, noch nie benutzt haben.
- Im Supply Chain Management können Administratoren alle gespeicherten Einstellungen einsehen und bearbeiten, auch für einzelne Arbeitskräfte. Diese Funktionalität kann ihnen bei der Fehlersuche oder der Feinabstimmung neuer Funktionen helfen.

> [!IMPORTANT]
> Die Funktion *Benutzereinstellungen für mobile Geräte* gilt nur für die neue mobile App Lagerortverwaltung. Sie funktioniert nicht mit der alten Lagerort App.

## <a name="turn-the-mobile-device-user-settings-feature-on-or-off"></a>Funktion für die Benutzereinstellungen für mobile Geräte ein- oder ausschalten

Um die in diesem Artikel beschriebene Funktionalität zu verwenden, muss die Funktion *Benutzereinstellungen, Symbole und Schritttitel für die neue Lagerort-App* für Ihr System aktiviert sein. Ab Supply Chain Management 10.0.25 ist diese Funktion obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.25 ausführen, können Administratoren diese Funktionalität ein- oder ausschalten, indem sie nach der Funktion *Benutzereinstellungen, Symbole und Schritttitel für die neue Lagerort-App* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

## <a name="create-and-manage-user-settings"></a>Benutzereinstellungen erstellen und verwalten

Verwenden Sie die Seite **Benutzereinstellungen für mobile Geräte**, um Einstellungsprofile auf allen Granularitätsebenen zu erstellen, anzuzeigen und zu verwalten. Wenn eine Arbeitskraft zum ersten Mal ihre Benutzereinstellungen auf einem neuen Gerät bearbeitet, wird auf dieser Seite automatisch ein neues Profil hinzugefügt, wenn es noch nicht vorhanden ist. Dieses Profil wird dann jedes Mal aktualisiert, wenn die Arbeitskraft eine Änderung vornimmt.

Sie können auch ein Einstellungsprofil festlegen, das für alle Marken, Gerätemodelle und/oder Arbeitskräfte gilt. Sie können dann die Granularität erhöhen, indem Sie spezifischere Einstellungen für einzelne Marken, Modelle und/oder Arbeitskräfte anwenden.

Folgen Sie diesen Schritten, um Benutzereinstellungen für Ihre mobilen Geräte zu erstellen und zu verwalten.

1. Gehen Sie zu **Warehouse Management \> Einrichtung \> Mobilgerät \> Benutzereinstellungen für Mobilgeräte**.
1. Wählen Sie ein bestehendes Benutzereinstellungsprofil im Listenbereich, um dessen Datensatz zu öffnen. Wählen Sie alternativ **Neu** im Aktivitätsbereich, um ein neues Profil zu erstellen.

    Jedes Profil im Listenbereich ist mit einem Label versehen, um die Marke, das Modell und/oder die Benutzer-ID anzugeben, für die das Profil gilt. Allgemeinere Profile haben einen Wert von *Alle* für einige oder alle dieser Merkmale.

1. Legen Sie im Kopfbereich des Datensatzes für das neue oder ausgewählte Einstellungsprofil die folgenden Felder fest:

    - **Gerätemarke** - Wählen Sie den Namen der Gerätemarke, für die das Profil gelten soll. Wenn das Profil für alle Marken gelten soll, lassen Sie dieses Feld leer. Die Liste der Werte enthält alle Marken, die in Ihrem System definiert wurden. Informationen darüber, wie Sie die Liste der Marken definieren, finden Sie im nächsten Abschnitt.
    - **Gerätemodell-ID** - Wählen Sie das Gerätemodell, für das das Profil gelten soll. Wenn das Profil für alle Modelle der gewählten Marke gelten soll, lassen Sie dieses Feld leer. Die Liste der Werte enthält alle Modelle, die für die Marke definiert wurden, die im Feld **Gerätemarke** ausgewählt ist. Informationen darüber, wie Sie die Liste der Modelle für jede Marke definieren, finden Sie im nächsten Abschnitt.
    - **Benutzer-ID** - Wählen Sie die Benutzer-ID der Arbeitskraft im Lagerort, für die das Einstellungsprofil gelten soll. Wenn das Profil für alle Arbeitskräfte gelten soll, lassen Sie dieses Feld leer.

1. Legen Sie im Inforegister **Allgemein** die folgenden Felder fest:

    - **Position der Schaltflächen** - Wählen Sie, wie die Schaltflächen auf dem Gerät positioniert werden sollen. Die Elemente in der App werden so verschoben, dass sie besser zu den Vorlieben oder der Händigkeit der Arbeitskraft passen. Die verfügbaren Optionen sind *Unten rechts (Standard)*, *Unten links*, *Oben rechts* und *Oben links*.
    - **Displayausrichtung** - Wählen Sie die Displayausrichtung, die standardmäßig in der App angewendet werden soll.
    - **Mit Kamera scannen** - Setzen Sie diese Option auf *Ja*, um die Gerätekamera zum Scannen von Eingabefeldern zu verwenden, bei denen der bevorzugte Eingabemodus auf *Scannen* festgelegt ist. Wenn Ihr Gerät über einen eingebauten Scanner verfügt, legen Sie diese Option auf *Nein* fest, um stattdessen den Scanner zu verwenden.
    - **Produktfoto anzeigen** - Wählen Sie, ob Produktfotos angezeigt werden sollen, wenn sie für das freigegebene Produkt verfügbar sind. Weitere Informationen zum Hinzufügen von Produktbildern finden Sie unter [Hinzufügen eines Bildes zu einem Produkt](../pim/tasks/add-image-product.md).
    - **Farbthema anzeigen** - Wählen Sie ein Farbthema für das Gerät.
    - **Tonpegel** - Wählen Sie den Tonpegel für das Gerät. Wählen Sie einen Wert zwischen 0 (Null) und 10. Ein Wert von *0* steht für keinen Ton, und ein Wert von *10* steht für maximale Lautstärke. Der Standardwert ist *4*.
    - **Vibrationspegel** - Wählen Sie den Vibrationspegel für das Gerät. Wählen Sie einen Wert zwischen 0 (Null) und 5. Ein Wert von *0* steht für keine Vibration, und ein Wert von *5* steht für maximale Vibration. Der Standardwert ist *1*.
    - **Textskalierung in Prozent** - Geben Sie die Textgröße als Prozentsatz der Standardgröße an. Geben Sie einen Wert zwischen 70 und 400 ein. Ein Wert von *70* steht für die kleinste Textskala und ein Wert von *400* für die größte Textskala. Der Standardwert ist *100*.
    - **Tastenskalierung in Prozent** - Geben Sie die Größe der Schaltfläche als Prozentsatz der Standardgröße an. Geben Sie einen Wert zwischen 50 und 200 ein. Ein Wert von *50* steht für die kleinste Schaltflächengröße und ein Wert von *200* für die größte Schaltflächengröße. Der Standardwert ist *100*.

## <a name="create-and-manage-mobile-device-brands"></a>Erstellen und Verwalten von Marken für mobile Geräte

Verwenden Sie die Seite **Mobilgerätemarken**, um die Gerätemarken und -modelle, die mit Ihren Einstellungsprofilen verwendet werden können, anzuzeigen, zu erstellen und zu verwalten. Die mobile App holt und sendet automatisch den lokalen Markennamen und die Modell-ID, wenn eine Arbeitskraft das erste Mal ihre Einstellungen auf einem bestimmten Gerät bearbeitet. Daher werden die meisten dieser Datensätze normalerweise automatisch generiert. Sie können jedoch auch alle Datensätze auf dieser Seite verwalten. Zum Beispiel können Sie jeder Marke und jedem Modell nützlichere Beschreibungen geben, um ähnliche oder kryptische Modell-IDs zu unterscheiden.

Folgen Sie diesen Schritten, um Ihre Marken und Modelle für mobile Geräte zu erstellen und zu verwalten.

1. Gehen Sie zu **Warehouse Management \> Einrichtung \> Mobiles Gerät \> Mobiles Gerät Marken**.
1. Wählen Sie im Listenbereich eine Marke für ein mobiles Gerät aus, um ihren Datensatz zu öffnen. Wählen Sie alternativ **Neu** im Aktivitätsbereich, um eine neue Marke zu erstellen.
1. Legen Sie im Kopfbereich des Datensatzes für die neue oder ausgewählte Gerätemarke die folgenden Felder fest:

    - **Gerätemarkenname** - Der Markenname des Geräts, z. B. *Microsoft Corporation*.
    - **Beschreibung** - Sie können eine Beschreibung eingeben, um die Marken zu unterscheiden.

1. Das Inforegister **Mobilgerätemodelle** zeigt alle Modelle für die ausgewählte Gerätemarke an. Verwenden Sie die Schaltflächen in der Symbolleiste, um dem Raster Zeilen hinzuzufügen oder Zeilen zu entfernen. Für jede Zeile können Sie die folgenden Felder festlegen:

    - **Gerätemodell-ID** - Die Gerätemodell-ID, z. B. *Surface Book 2*.
    - **Beschreibung** - Sie können eine Beschreibung eingeben, um die Modell-IDs zu unterscheiden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Mobile Lagerortsverwaltungs-App installieren und verbinden](install-configure-warehouse-management-app.md)
- [Weisen Sie der mobilen Warehouse Management-App Schrittsymbole und -titel zu](step-icons-titles.md)