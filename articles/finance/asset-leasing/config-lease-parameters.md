---
title: Mietvertragsparameter konfigurieren (Vorschau)
description: In diesem Thema werden die Konfigurationseinstellungen für Anlagenleasing beschrieben, z. B. Sicherheitsinformationen und Buchhaltungseinstellungen.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2a644b3c9d9ed4fc86a816af1ab338b96b1aa7ad
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968076"
---
# <a name="configure-lease-parameters"></a>Mietvertragsparameter konfigurieren

[!include [banner](../includes/banner.md)]

Verschiedene Konfigurationseinstellungen wirken sich auf das Verhalten von Anlagenleasing aus. Diese Einstellungen umfassen Erfassungsnamen, allgemeine Parameter und Buchungsprofileinstellungen.

1. Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Anlagenleasing-Parameter**.
2. Wählen Sie auf der Registerkarte **Mietverträge** das Inforegister **Allgemein**.

    Der **Manuelles Überschreiben der Klassifizierung zulassen**-Parameter bestimmt, ob die Mietvertragsklassifizierung überschrieben werden kann, bevor der Zahlungsplan bestätigt wird.

    Der **Entitätsübergreifender Batch**-Parameter bestimmt, ob Sie von der aktuellen juristischen Person auf andere juristische Personen buchen können. Wenn dieser Parameter aktiviert ist, können Sie Journaleinträge für die juristischen Personen erstellen, auf die Sie Zugriff haben.

3. Stellen Sie die **Löschung bestätigter Mietverträge zulassen**-Option auf **Ja** fest, damit Mietverträge mit bestätigten Zahlungsplänen gelöscht werden können. Mietverträge können, unabhängig von der Einstellung dieser Option, nicht gelöscht werden, wenn gebuchte oder nicht gebuchte Transaktionen mit ihnen verknüpft sind. Sie können einen Mietvertragsdatensatz nach dem Löschen nicht wiederherstellen. Wenn Sie Datensätze für einen gelöschten Mietvertrag entweder manuell oder über Dateneinheiten hochladen, werden die hochgeladenen Informationen als neu behandelt und nicht als Aktualisierung eines vorhandenen Mietvertrags.

    Wenn Sie diese Option auf **Ja** setzen, und die Übergangsart des Buches **Kumulative Aufholoption A oder B** ist, setzt das System das **Zinssatz für Neukredit**-Feld auf der Seite **Bucheinrichtung** auf den Wert des **Zinssatz für Neukredit bei Übergang**-Felds. Wenn diese Option auf **Nein** gesetzt ist, wird der Zinssatz für den Hauptmietvertrag auf den Wert vom Feld **Zinssatz für Neukredit** auf der **Buchdetails**-Seite festgelegt, unabhängig von der Übergangsart des Buches.

4. Stellen Sie die **Abschreibungen für geschlossene Bücher zulassen**-Option auf **Ja**, damit Abschreibungsaufwendungen rückgängig gemacht werden können. Aufwandstransaktionen können auch bei geschlossener Buchversion rückgängig gemacht werden.

    > [!NOTE]
    > Wir empfehlen, diese Option auf **Nein** zu setzen. Die Einstellung dieser Option wird als Validierung und Kontrolle verwendet, um zu verhindern, dass eine geschlossene Buchversion versehentlich abgeschrieben wird. Indem Sie die Option auf **Nein** setzen, tragen Sie dazu bei, den Nettobuchwert und zukünftige Abschreibungsberechnungen korrekt zu halten.

5. Stellen Sie die **Aufschlüsselung des Zahlungsbetrags zulassen**-Option auf **Ja**, um eine Aufschlüsselung der Zahlungsbeträge auf dem **Zahlungsplanpositionen**-Inforegister der **Mieten**-Seite zu ermöglichen. Die Zahlungsaufschlüsselungstypen sind unter **Einstellen** auf der **Zahlungsbetragstypen**-Seite definiert. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
