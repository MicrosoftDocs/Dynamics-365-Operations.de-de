---
title: Statische Dateien hochladen und bereitstellen
description: In diesem Artikel wird beschrieben, wie Sie eine statische Datei im Microsoft Dynamics 365 Commerce Site Builder hochladen, und wie Sie eine benutzerdefinierte URL und Dateiname erstellen, die für die Anforderung dieser Datei verwendet werden können.
author: StuHarg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a1b14feba1466c3a5efc3b0ea66f20e9e818a8a5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885321"
---
# <a name="upload-and-serve-static-files"></a>Statische Dateien hochladen und bereitstellen

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie eine statische Datei im Microsoft Dynamics 365 Commerce Site Builder hochladen, und wie Sie eine benutzerdefinierte URL und Dateiname erstellen, die für die Anforderung dieser Datei verwendet werden können.

Bei einigen Connectors von Drittanbietern muss eine Datei von der E-Commerce-Website gehostet und von ihr aus bereitgestellt werden. Diese Connectors erwarten, dass die Datei durch Anforderungen an einen bestimmten Rückruf-URL-Pfad und Dateinamen zurückgegeben wird. In diesem Artikel wird daher erläutert, wie Sie eine statische Datei mit einer benutzerdefinierbaren URL und einem Dateinamen auf eine statische Dynamics 365 Commerce-E-Commerce-Website hochladen und auf dieser bedienen.

## <a name="create-a-site-url-that-returns-a-static-file"></a>Eine Website-URL erstellen, die eine statische Datei zurückgibt

Führen Sie diese Schritte aus, um eine Website-URL zu erstellen, die eine statische Datei im Commerce-Website-Generator zurückgibt.

1. Wechseln Sie zur Medienbibliothek Ihrer Website und laden Sie die Datei hoch, die durch Anforderungen an die URL bedient werden soll, die Sie definieren werden. Wenn Sie die Datei bereits hochgeladen haben, können Sie diesen Schritt überspringen.
1. Wechseln Sie zu **URLs** für Ihre Website.
1. Wählen Sie **Neu \> Neue URL** aus.
1. Im Dialogfeld **Neue URL** wählen Sie **Medienbibliotheksobjekt** aus.
1. Geben Sie im Feld **URL-Pfad** den URL-Pfad ein. Fügen Sie den Dateinamen in den Pfad ein.
1. Wählen Sie **Weiter**. Die Medienbibliothek wird geöffnet und zeigt alle Medienobjekte des Typs **Dokument** an, die hochgeladen wurden.
1. Wählen Sie die Datei aus, die für Anforderungen an die von Ihnen in Schritt 5 definierte URL bedient werden soll.
1. Wählen Sie **Speichern** aus.

An diesem Punkt ist die URL, die Sie erstellt haben, in einem Entwurfzustand. Die Datei, auf die die URL verweist, wird erst zurückgegeben, wenn Sie die URL veröffentlichen. Bevor Sie die URL veröffentlichen, können Sie überprüfen, ob sie die richtigen Daten zurückgibt.

## <a name="validate-and-publish-a-url"></a>Eine URL überprüfen und veröffentlichen

Gehen Sie folgendermaßen vor, um eine URL zu überprüfen, bevor Sie diese veröffentlichen.

1. Wechseln Sie zu **URLs** für Ihre Website und wählen Sie die URL für die Vorschau aus.
2. Im Eigenschaftenbereich rechts unter der Schaltfläche **Bearbeiten** wählen Sie den richtigen URL-Link aus. Ein neues Browserfenster wird geöffnet und Sie sollten einen Fehler 404 erhalten.
3. Fügen Sie die Abfragezeichenfolge **?preview=inprogress** an die URL an (z. B. `https://yoursite.com/callback.html?preview=inprogress`) und laden Sie die Seite neu. Die Datei, die Sie in die Medienbibliothek hochgeladen haben, sollte in der Antwort zurückgegeben werden.

Nachdem Sie die URL überprüft haben, können Sie sie veröffentlichen.

1. Wechseln Sie zu **URLs** für Ihre Website und wählen Sie die URL aus.
2. Wählen Sie in der Befehlsleiste **Veröffentlichen** aus.

## <a name="update-the-file-that-a-url-points-to"></a>Aktualisieren Sie die Datei, auf die eine URL verweist

Nachdem eine URL veröffentlicht wurde, können Sie sie aktualisieren, sodass sie auf eine andere Datei verweist. Alternativ können Sie die URL aktualisieren, damit sie auf einen anderen Ressourcentyp zeigt, wie im nächsten Abschnitt beschrieben. Sie können zum Beispiel mit der URL auf eine interne Seite oder eine Umleitung zeigen.

Führen Sie die folgenden Schritte aus, um die Datei zu aktualisieren, auf die eine URL zeigt.

1. Wechseln Sie zu **URLs** für Ihre Website und wählen Sie die URL für die Aktualisierung aus.
1. Wählen Sie im Eigenschaftenbereich rechts **Bearbeiten** aus.
1. Unter **URL-Zuweisung**, aktivieren Sie das Feld **Schritt 2** und wählen Sie dann ein neues Dokument aus der Medienbibliothek aus.
1. Wählen Sie **Anwenden** aus.

## <a name="update-the-asset-type-that-a-url-points-to"></a>Aktualisieren Sie den Objekttyp, auf den eine URL zeigt

Sie können auch eine URL aktualisieren, damit sie auf einen anderen Objekttyp (Ressource) verweist, wie z. B. eine interne Seite oder eine Umleitung.

Führen Sie diese Schritte aus, um den Objekttyp zu aktualisieren, auf den eine URL zeigt.

1. Wechseln Sie zu **URLs** für Ihre Website und wählen Sie die URL für die Aktualisierung aus.
1. Wählen Sie im Eigenschaftenbereich rechts **Bearbeiten** aus.
1. Unter **URL-Zuweisung** unter **Schritt 1** wählen Sie einen anderen Objekttyp aus.
1. Aktivieren Sie das Feld **Schritt 2**, und wählen Sie dann das neue Objekt aus.
1. Wählen Sie **Anwenden** aus.

## <a name="change-the-url-path"></a>Ändern Sie den URL-Pfad

Nachdem eine URL erstellt wurde, kann ihr Pfad nicht mehr geändert werden. Wenn Sie einen URL-Pfad ändern müssen, der eine Datei oder irgendeinen anderen Ressourcentyp bedient, müssen Sie eine neue URL erstellen, sie einer vorhandenen Datei oder anderen Ressource zuordnen und dann die Veröffentlichung aufheben und die alte URL löschen.

Folgen Sie diesen Schritte, um den URL-Pfad zu ändern.

1. Um eine neue URL zu erstellen und sie zur vorhandenen Datei oder einer anderen Ressource zuzuordnen, folgen Sie den Anleitungen im Abschnitt [Eine Website-URL erstellen, die eine statische Datei zurückgibt](#create-a-site-url-that-returns-a-static-file) weiter oben in diesem Artikel.
1. Wählen Sie die neue URL aus und wählen Sie dann **Veröffentlichen** in der Befehlsleiste aus. Die neue URL wird veröffentlicht.
1. Um die Veröffentlichung der alten URL aufzuheben, wählen Sie sie aus und wählen Sie dann **Veröffentlichung aufheben** in der Befehlsleiste aus. Sie können jetzt die alte URL löschen, wenn Sie dies möchten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die Verwaltung digitaler Anlagen](dam-overview.md)

[Bilder hochladen](dam-upload-images.md)

[Videos hochladen](dam-upload-video.md)

[Andere Dateien außer Bildern und Videos hochladen](dam-upload-files.md)

[Bilder zuschneiden](dam-crop-images.md)

[Bildfokuspunkte anpassen](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]