---
title: Robots.txt-Dateien verwalten
description: In diesem Thema wird beschrieben, wie Sie robots.txt-Dateien in Microsoft Dynamics 365 Commerce verwalten.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: afd7982179dc9845c9adc24e8c7c9951a04460a3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477707"
---
# <a name="manage-robotstxt-files"></a>Robots.txt-Dateien verwalten

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie robots.txt-Dateien in Microsoft Dynamics 365 Commerce verwalten.

Der Robots-Ausschlussstandard oder robots.txt ist ein Standard, den Websites für die Kommunikation mit Webrobotern verwenden. Er weist Webroboter an, welche Bereiche einer Website nicht besucht werden sollten. Roboter werden häufig von Suchmaschinen verwendet, um Websites zu indizieren.

Um Roboter von einem Server auszuschließen, erstellen Sie eine Datei auf dem Server. In dieser Datei geben Sie eine Zugriffsrichtlinie für Roboter an. Die Datei muss über HTTP unter der lokalen URL **/robots.txt** erreichbar sein. Mithilfe der robots.txt-Datei können Suchmaschinen den Inhalt Ihrer Website indizieren.

Mit Dynamics 365 Commerce können Sie eine robots.txt-Datei für Ihre Domain hochladen. Für jede Domain in Ihrer Commerce-Umgebung können Sie eine robots.txt-Datei hochladen und dieser Domain zuordnen.

Weitere Informationen zur robots.txt-Datei finden Sie unter [Die Web Robots-Seiten](https://www.robotstxt.org/).

## <a name="upload-a-robotstxt-file"></a>Laden Sie eine robots.txt-Datei hoch

Stellen Sie sicher, nachdem Sie Ihre robots.txt-Datei gemäß dem [Roboter-Ausschlussstandard](https://www.robotstxt.org/orig.html) erstellt und bearbeitet haben, dass die Datei auf dem Computer zugänglich ist, auf dem Sie auch die Commerce-Authoring-Tools verwenden. Die Datei muss **robots.txt** genannt werden. Für beste Ergebnisse muss es das Format haben, das in der Norm angegeben ist. Jeder Commerce-Kunde ist für die Validierung und Pflege des Inhalts seiner robots.txt-Datei verantwortlich. Um eine robots.txt-Datei hochzuladen, müssen Sie als Systemadministrator bei Commerce angemeldet sein.

Gehen Sie folgendermaßen vor, um eine robots.txt-Datei in Commerce hochzuladen.

1. Melden Sie sich bei Commerce als Systemadministrator an.
2. Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen** (neben dem Zahnradsymbol) aus, um es zu erweitern.
3. Wählen Sie unter **Mandanteneinstellungen** die Option **Robots.txt** aus. Eine Liste aller Ihrer Umgebung zugeordneten Domänen wird im Hauptteil des Fensters angezeigt.
4. Wählen Sie **Verwalten** aus, um eine robots.txt-Datei für eine Domäne in Ihrer Umgebung hochzuladen.
5. Wählen Sie im rechten Menü **Hochladen** (den nach oben zeigenden Pfeil) neben der Domäne aus, die der robots.txt-Datei zugewiesen ist. Ein Dateibrowser-Dialogfeld wird angezeigt.
6. Navigieren Sie im Dialogfeld zu der robots.txt-Datei, die Sie für die zugeordnete Domäne hochladen möchten, und wählen Sie dann **Öffnen** aus, um den Upload abzuschließen.

> [!NOTE] 
> Während des Uploads überprüft Commerce, ob es sich bei der Datei um eine Textdatei handelt, überprüft jedoch nicht den Inhalt der Datei.

## <a name="download-a-robotstxt-file"></a>Laden Sie eine robots.txt-Datei hoch

Gehen Sie folgendermaßen vor, um eine robots.txt-Datei in Commerce herunterzuladen.

1. Melden Sie sich bei Commerce als Systemadministrator an.
2. Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen** (neben dem Zahnradsymbol) aus, um es zu erweitern.
3. Wählen Sie unter **Mandanteneinstellungen** die Option **Robots.txt** aus. Eine Liste aller Ihrer Umgebung zugeordneten Domänen wird im Hauptteil des Fensters angezeigt.
4. Wählen Sie **Verwalten** aus, um eine robots.txt-Datei für eine Domäne in Ihrer Umgebung herunterzuladen.
5. Wählen Sie rechts im Menü die Schaltfläche **Herunterladen** aus (der nach unten zeigende Pfeil) neben der Domäne, die der robots.txt-Datei zugeordnet ist. Ein Dateibrowser-Dialogfeld wird angezeigt.
6. Navigieren Sie im Dialogfeld zum gewünschten Speicherort auf Ihrem lokalen Laufwerk, bestätigen Sie einen Dateinamen oder geben Sie einen ein. Wählen Sie dann **Speichern** aus, um den Download abzuschließen.

> [!NOTE]
> Mit diesem Verfahren können nur robots.txt-Dateien heruntergeladen werden, die zuvor mit den Commerce-Authoring-Tools hochgeladen wurden.

## <a name="delete-a-robotstxt-file"></a>Laden Sie eine robots.txt-Datei hoch

Gehen Sie folgendermaßen vor, um eine robots.txt-Datei in Commerce zu löschen.

1. Melden Sie sich bei Commerce als Systemadministrator an.
2. Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen** (neben dem Zahnradsymbol) aus, um es zu erweitern.
3. Wählen Sie unter **Mandanteneinstellungen** die Option **Robots.txt** aus. Eine Liste aller Ihrer Umgebung zugeordneten Domänen wird im Hauptteil des Fensters angezeigt.
4. Wählen Sie **Verwalten** aus, um eine robots.txt-Datei für eine Domäne in Ihrer Umgebung zu löschen.
5. Wählen Sie im Menü rechts die Schaltfläche **Löschen** (das Papierkorb-Symbol) neben der Domäne aus, die der robots.txt-Datei zugeordnet ist. Ein Dateibrowserfenster wird angezeigt.
6. Navigieren Sie im Dateibrowser-Fenster zu der robots.txt-Datei, die Sie für die Domäne löschen möchten, wählen Sie sie aus und klicken Sie dann auf **Öffnen**. Eine Warnmeldung wird angezeigt.
7. Wählen Sie im Nachrichtenfeld **Löschen** aus, um das Löschen der robots.txt-Datei zu bestätigen.

> [!NOTE] 
> Mit diesem Verfahren können nur robots.txt-Dateien gelöscht werden, die zuvor mit den Commerce-Authoring-Tools hochgeladen wurden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Domänennamen konfigurieren](configure-your-domain-name.md)

[Neuen E-Commerce-Mandanten bereitstellen](deploy-ecommerce-site.md)

[E-Commerce-Website erstellen](create-ecommerce-site.md)

[Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal](associate-site-online-store.md)

[URL-Umleitungen in Massen hochladen](upload-bulk-redirects.md)

[B2C-Mandanten in Commerce einrichten](set-up-B2C-tenant.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

[Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung](configure-multi-B2C-tenants.md)

[Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
