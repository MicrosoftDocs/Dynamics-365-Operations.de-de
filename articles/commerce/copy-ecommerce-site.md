---
title: Kopieren einer E-Commerce-Website
description: In diesem Artikel wird beschrieben, wie Sie eine bestehende E-Commerce-Website innerhalb von oder zwischen E-Commerce-Umgebungen in Microsoft Dynamics 365 Commerce Site Builder kopieren.
author: josaw1
ms.date: 06/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 9b74e0d48be29272b893c855c229e4003f0c161e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276291"
---
# <a name="copy-an-e-commerce-site"></a>Kopieren einer E-Commerce-Website

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie eine bestehende E-Commerce-Website innerhalb von oder zwischen E-Commerce-Umgebungen in Microsoft Dynamics 365 Commerce Site Builder kopieren.

Dynamics 365 Commerce unterstützt das Kopieren oder Klonen von Websites als Selbstbedienungsvorgang in Commerce Site Builder. Websites können innerhalb einer einzigen E-Commerce Umgebung oder zwischen zwei E-Commerce Umgebungen kopiert werden. Der Benutzer, der den Vorgang des Kopierens der Website initiiert, muss sowohl in der E-Commerce Umgebung der Quelle als auch des Ziels ein Mandant-Administrator sein.

Der Vorgang Website kopieren kopiert den gesamten E-Commerce-Inhalt der Ausgangsseite. Dieser Inhalt umfasst Seiten, Fragmente, Vorlagen, URLs und Assets. Bevor eine neue Seite verwendet werden kann, muss sie durch den Prozess des ersten Ausführens (FRE) initialisiert werden. Kanäle können im Site Builder unter **Site-Einstellungen \> Kanäle** zugeordnet und verwaltet werden.

Die Dauer des Vorgangs zum Kopieren der Site hängt in erster Linie von der Anzahl der Assets auf der Quell-Site ab. Für außergewöhnlich große Sites empfehlen wir Ihnen, stattdessen den Vorgang Umgebung kopieren zu verwenden. (Dieser Vorgang wird auch als Datenportabilitätsvorgang bezeichnet).

> [!NOTE]
> - Die Ausgangsseite ist für die Dauer des Kopiervorgangs schreibgeschützt.
> - Es werden nur veröffentlichte Versionen von Dokumenten kopiert. Wenn keine Versionen veröffentlicht wurden, werden nur die neuesten Versionen übernommen.
> - Der Versionsverlauf für Inhalte ist auf der Zielsite nicht verfügbar.

## <a name="copy-a-site-within-an-e-commerce-environment"></a>Kopieren einer Website innerhalb einer E-Commerce Umgebung

Um eine Website innerhalb einer E-Commerce Umgebung zu kopieren, führen Sie diese Schritte aus.

1. Melden Sie sich beim Site Builder für die Umgebung an, in der Sie den Kopiervorgang durchführen möchten.
1. Öffnen Sie die Site-Listenansicht, indem Sie in der oberen rechten Ecke **Site Switcher** und dann **Sites verwalten** wählen.
1. Suchen Sie den Standort, den Sie kopieren oder klonen möchten, und wählen Sie ihn aus, indem Sie das Kontrollkästchen neben dem Standortnamen aktivieren.
1. Wählen Sie in der Befehlsleiste **Site kopieren** aus.
1. Geben Sie im Flyoutmenü **Site kopieren** in das Feld **Neuer Site-Name** einen Namen für die neue Site ein. Der neue Site-Name muss in der E-Commerce Umgebung eindeutig sein. Die Felder **Quellmieter** und **Quellstandort** werden automatisch auf die Informationen für den aktuellen Mandanten und den ausgewählten Standort festgelegt.
1. Wählen Sie **Kopie erstellen**.

Nach der Überprüfung der Informationen zeigt eine Benachrichtigung an, dass ein neuer Auftrag zum Kopieren der Website erstellt wurde. Sie können den Fortschritt des Auftrags im [rechten Fensterbereich der Seite **Mandantenaufträge** überwachen](#monitor-the-site-copy-operation). Wenn der Kopiervorgang erfolgreich abgeschlossen wurde, wird der neue Standort in der Liste der Standorte in der Standortlistenansicht angezeigt.

Die folgende Abbildung zeigt ein Beispiel für das Flyoutmenü **Site kopieren** in Site Builder.

![Flyoutmenü Site kopieren im Site Builder.](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>Kopieren einer Site zwischen zwei E-Commerce Umgebungen

Um eine Website zwischen zwei E-Commerce Umgebungen zu kopieren, gehen Sie folgendermaßen vor.

1. Melden Sie sich beim Site Builder für die E-Commerce Umgebung des Ziels an.
1. Wählen Sie in der Befehlsleiste **Site kopieren** aus.
1. Geben Sie im Flyoutmenü **Site kopieren** in das Feld **Neuer Site-Name** einen Namen für die neue Site ein. Der neue Site-Name muss in der E-Commerce Umgebung eindeutig sein.
1. Wählen Sie im Feld **Quell-Mandant** den Namen des Quell-Mandanten.
1. Wählen Sie im Feld **Quellstandort** den Quellstandort.
1. Wählen Sie **Kopie erstellen**.

> [!NOTE]
> Die Berechtigungen des Mandanten-Administrators sind sowohl für die E-Commerce Umgebung der Quelle als auch des Ziels erforderlich.

Nach der Überprüfung der Informationen zeigt eine Benachrichtigung an, dass ein neuer Auftrag zum Kopieren der Website erstellt wurde. Sie können den Fortschritt des Auftrags im [rechten Fensterbereich der Seite **Mandantenaufträge** überwachen](#monitor-the-site-copy-operation). Wenn der Kopiervorgang erfolgreich abgeschlossen wurde, wird der neue Standort in der Liste der Standorte in der Standortlistenansicht angezeigt.

## <a name="map-channels-during-the-site-copy-operation-optional"></a>Zuordnen von Kanälen während des Site-Kopiervorgangs (optional)

Quellkanäle und Gebietsschemata können als Teil des Site-Kopiervorgangs Zielkanälen und Gebietsschemata zugeordnet werden. Wenn die Kanalzuordnung als Teil des Site-Kopiervorgangs erfolgt, sind das Initialisieren der Site mit dem FRE-Prozess und das Konfigurieren der Kanäle in den Site-Einstellungen nicht erforderlich. 

Führen Sie die folgenden Schritte aus, um alle Kanäle und Gebietsschemas "wie sie sind" (1-zu-1) im Site Builder zuzuordnen.

1. Öffnen Sie die Site-Listenansicht, indem Sie in der oberen rechten Ecke **Site Switcher** und dann **Sites verwalten** wählen.
1. Suchen Sie den Standort, den Sie kopieren oder klonen möchten, und wählen Sie ihn aus, indem Sie das Kontrollkästchen neben dem Standortnamen aktivieren.
1. Wählen Sie in der Befehlsleiste **Site kopieren** aus.
1. In dem **Website kopieren** Flyout-Menü, geben Sie Werte für **Neuer Seitenname**, **Quellenmieter** und **Quellseite** ein (falls noch nicht vorhanden).
1. Wählen Sie **Kanalzuordnung hinzufügen** aus.
1. In dem Flyout-Menü **Konfigurieren Sie Site-Kanäle und Gebietsschemas** wählen Sie **Quellkanal**, und wählen Sie dann den Quellkanal aus.  
1. Wählen Sie **Zielkanal** und dann denselben Kanal wie den Quellkanal aus. 
1. Wählen Sie **Gebietsschema hinzufügen** aus.
1. Wählen Sie **Quellgebietsschema** und dann das Quellgebietsschema aus.
1. Wählen Sie **Zielgebietsschema** und dann denselben Gebietsschema wie das Quellgebietsschema aus. 
1. Zum **URL-Pfad** geben Sie einen eindeutigen URL-Pfad ein, der derzeit nicht in der Zielumgebung verwendet wird.
1. Wiederholen Sie die Schritte 8 bis 11 für jedes Gebietsschema, das dem Kanal zugeordnet werden soll.
1. Wählen Sie **Anwenden** aus.
1. Wiederholen Sie die Schritte 6 bis 11 für jeden Quellkanal.
1. Wählen Sie **Schließen** aus.
1. Überprüfen Sie die Konfiguration auf Genauigkeit und wählen Sie dann **Website kopieren** aus.

> [!NOTE]
> Alle Quellkanäle und Gebietsschemas müssen zugeordnet werden und können nur einmal zugeordnet werden.

## <a name="monitor-the-site-copy-operation"></a>Monitor des Vorgangs der Standortkopie

Um den Fortschritt des Vorgangs zum Kopieren der Website zu überwachen, gehen Sie folgendermaßen vor.

1. Melden Sie sich beim Site Builder für die E-Commerce Umgebung des Ziels an.
1. Wählen Sie im linken Fensterbereich **Mandantenaufträge**.
1. Auf der Seite **Aufträge für Mandanten** suchen Sie den Auftrag für die Standortkopie in der Liste und wählen ihn aus. Auf der rechten Seite erscheint ein Fenster mit dem Status und den Details des ausgewählten Auftrags.

Sie können einen Auftrag abbrechen, der den Status **In Bearbeitung** hat. Markieren Sie den Auftrag in der Liste und wählen Sie dann **Abbrechen** auf der Befehlsleiste.

Sie können einen Auftrag mit dem Status **Fehlgeschlagen** oder **Mit Fehlern abgeschlossen** erneut versuchen. Markieren Sie den Auftrag in der Liste und wählen Sie dann auf der Befehlsleiste **Wiederaufnahme**.

> [!NOTE]
> Die Verarbeitung von Video-Assets kann nach Abschluss eines Kopierauftrags vor Ort fortgesetzt werden.

Die folgende Abbildung zeigt ein Beispiel für den rechten Bereich der Seite **Mandanten Aufträge** in Site Builder.

![Auftragsdetails im rechten Fensterbereich der Seite Aufträge für Mandanten im Site Builder.](media/site-copy_2.png)

## <a name="initialize-a-new-site-by-using-the-fre-process"></a>Initialisieren Sie eine neue Website mit Hilfe des FRE-Prozesses

Bevor die neue Seite verwendet werden kann, muss sie durch den FRE-Prozess initialisiert werden.

Führen Sie die folgenden Schritte aus, um eine neue Website mit Hilfe des FRE-Prozesses zu initialisieren.

1. Melden Sie sich beim Website-Builder für die neue Website an.
1. Öffnen Sie die Site-Listenansicht, indem Sie in der oberen rechten Ecke **Site Switcher** und dann **Sites verwalten** wählen.
1. Suchen und wählen Sie die neue Site, die Sie initialisieren möchten.
1. Wählen Sie in der Dialogbox **Einrichtung Ihrer Site** im Feld **Wählen Sie eine Domäne** eine Domäne aus. Alle Domänen, die während der Initialisierung mit der E-Commerce Umgebung verknüpft wurden, stehen zur Auswahl.
1. Wählen Sie im Feld **Wählen Sie einen Standardkanal** den zugehörigen Online Store Kanal. Der ausgewählte Channel stellt Sortimente und andere Informationen bereit, die in der Commerce-Zentrale gespeichert sind.
1. Wählen Sie im Feld **Wählen Sie eine Standardsprache** die Standard-Authoring-Sprache aus. Alle Sprachen, die für den ausgewählten Online Store-Kanal konfiguriert wurden, stehen zur Auswahl.
1. Im Feld **Pfad** besteht der Wert aus der Basisdomäne und einem optionalen URL-Pfad, den Sie eingeben können. Sie können den URL-Pfad leer lassen, wenn der Channel vom Stammverzeichnis der Domäne aus bedient wird, oder wenn Sie diese Informationen später in der Channel-Konfigurationsansicht im Site Builder eingeben möchten. Der Pfad der Website muss in der E-Commerce Umgebung eindeutig sein.
1. Wählen Sie **OK** aus. Die Website wird mit den von Ihnen angegebenen Informationen initialisiert und Sie werden zur Website-Verwaltungsansicht weitergeleitet.

Die folgende Abbildung zeigt ein Beispiel für das Dialogfeld **Site einrichten** im Site Builder.

![Einrichtung des Dialogfelds für Ihre Website im Site Builder.](media/site-copy_3.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Domänennamen konfigurieren](configure-your-domain-name.md)

[Neuen E-Commerce-Mandanten bereitstellen](deploy-ecommerce-site.md)

[Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal](associate-site-online-store.md)

[Robots.txt-Dateien verwalten](manage-robots-txt-files.md)

[URL-Umleitungen in Massen hochladen](upload-bulk-redirects.md)

[Einrichten eines B2C-Mandanten in Commerce](set-up-b2c-tenant.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

[Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung](configure-multi-b2c-tenants.md)

[Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)
