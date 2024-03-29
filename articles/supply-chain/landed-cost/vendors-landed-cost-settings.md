---
title: Lieferanteneinstellungen für kalkulierte Gesamttransportkosten hinzugefügt
description: Dieser Artikel beschreibt die neuen Felder, die der bestehenden Seite „Lieferanten“ hinzugefügt werden, wenn Sie das Modul „Gesamttransportkosten“ aktivieren. Sie verwenden diese Felder, um die Lieferanten festzulegen, die Sie zusammen mit den Funktionen für kalkulierte Gesamttransportkosten verwenden werden.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 84d1dee0815b036a3d411eabff49d8a08249bed3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882575"
---
# <a name="vendor-settings-added-for-landed-cost"></a>Lieferanteneinstellungen für kalkulierte Gesamttransportkosten hinzugefügt

[!include [banner](../../includes/banner.md)]

Wenn Sie das Modul **Gesamttransportkosten** aktivieren, werden der bestehenden Seite **Lieferanten** mehrere neue Felder hinzugefügt. Sie verwenden diese Felder, um die Lieferanten festzulegen, die Sie zusammen mit den Funktionen für kalkulierte Gesamttransportkosten verwenden werden.

Um die entsprechenden Felder festzulegen, gehen Sie zu **Beschaffung und Bezugsquellenfindung \> Lieferanten \> Alle Lieferanten**. Öffnen Sie einen bestehenden Lieferanten oder erstellen Sie einen neuen Lieferanten und wählen Sie dann das Inforegister **Sonstige Details**. Alle neuen Felder, die das Modul **Gesamttransportkosten** hinzufügt, erscheinen unter der Überschrift **Fahrten**. Die folgende Tabelle beschreibt diese Felder.

| Feld | Beschreibung |
|---|---|
| Versandart | <p>Wählen Sie die Rolle des Anbieters in Bezug auf die Gesamttransportkosten:</p><ul><li>**Keine** - Der Lieferant hat keine spezifische Rolle, die sich auf die Gesamttransportkosten bezieht. Dieser Wert ist die Standardeinstellung, da die meisten Lieferanten wahrscheinlich keine spezifische Rolle haben werden.</li><li>**Versandfirma** - Der Lieferant ist eine Versandfirma. Lieferanten, die diese Schifffahrtsart haben, stehen zur Auswahl im Feld **Schifffahrtsfirma** auf der Seite **Fahrten**.</li><li>**Zoll Broker** - Der Anbieter ist ein Zoll Broker. Lieferanten, die diese Versandart haben, stehen auf der Seite **Paletten** im Feld **Zoll Broker** zur Auswahl.</li><li>**Agent** - Der Lieferant ist ein Agent. Lieferanten, die diese Versandart haben, stehen auf den Seiten **Lieferanten** und **Einkaufsbestellungen** im Feld **Vertreter** zur Auswahl.</li></ul> |
| Kostentypgruppe | Weisen Sie den Lieferanten einer Kostenartengruppe zu, um [Autokalkulation](auto-cost-setup.md) auszuwählen. |
| Von-Port | Wählen Sie den Herkunftshafen für die Fahrt. |
| Agent | Der Standardbevollmächtigte, wenn Käufe beim Lieferanten getätigt werden. |
| Nachkalkulationskreditor importieren | <p>Geben Sie an, ob es sich bei dem Anbieter um einen Anbieter mit kalkulierten Gesamttransportkosten handelt.</p><p>**Tipp:** Sie können dieses Feld zusammen mit der Sicherheit auf Datensatzebene verwenden, um die Einkaufsbestellungen einzuschränken, die angezeigt werden, wenn eine Fahrt erstellt wird.</p> |
| Versandunternehmen | Wählen Sie die Standardversandfirma, die beim Erstellen von Einkaufsbestellungen für den Lieferanten verwendet wird. |
| Dienstanbieter | Geben Sie an, ob der Lieferant ein Servicesanbieter ist. |
| Über-/Untertoleranzgruppe | Wählen Sie die standardmäßige Über/Unter-Toleranzgruppe für den Lieferanten aus. |
