---
title: Kopieren einer E-Commerce-Website
description: In diesem Thema wird beschrieben, wie Sie eine bestehende E-Commerce-Website innerhalb von oder zwischen E-Commerce-Umgebungen in Microsoft Dynamics 365 Commerce Site Builder kopieren.
author: psimolin
ms.date: 03/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 284a33099fecc5a8e8d5d5d31612abab51735773
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8386979"
---
# <a name="copy-an-e-commerce-site"></a>Kopieren einer E-Commerce-Website

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

In diesem Thema wird beschrieben, wie Sie eine bestehende E-Commerce-Website innerhalb von oder zwischen E-Commerce-Umgebungen in Microsoft Dynamics 365 Commerce Site Builder kopieren.

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
1. Wählen Sie im Aktionsbereich **Seite kopieren**.
1. Geben Sie im Dialogfeld **Site kopieren** in das Feld **Neuer Site-Name** einen Namen für die neue Site ein. Der neue Site-Name muss in der E-Commerce Umgebung eindeutig sein. Die Felder **Quellmieter** und **Quellstandort** werden automatisch auf die Informationen für den aktuellen Mandanten und den ausgewählten Standort festgelegt.
1. Wählen Sie **Kopie erstellen**.

Nach der Überprüfung der Informationen zeigt eine Benachrichtigung an, dass ein neuer Auftrag zum Kopieren der Website erstellt wurde. Sie können den Fortschritt des Auftrags im [rechten Fensterbereich der Seite **Mandantenaufträge** überwachen](#monitor-the-site-copy-operation). Wenn der Kopiervorgang erfolgreich abgeschlossen wurde, wird der neue Standort in der Liste der Standorte in der Standortlistenansicht angezeigt.

Die folgende Abbildung zeigt ein Beispiel für das Dialogfeld **Site kopieren** in Site Builder.

![Dialogfeld Site kopieren im Site Builder.](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>Kopieren einer Site zwischen zwei E-Commerce Umgebungen

Um eine Website zwischen zwei E-Commerce Umgebungen zu kopieren, gehen Sie folgendermaßen vor.

1. Melden Sie sich beim Site Builder für die E-Commerce Umgebung des Ziels an.
1. Wählen Sie im Aktionsbereich **Seite kopieren**.
1. Geben Sie im Dialogfeld **Site kopieren** in das Feld **Neuer Site-Name** einen Namen für die neue Site ein. Der neue Site-Name muss in der E-Commerce Umgebung eindeutig sein.
1. Wählen Sie im Feld **Quell-Mandant** den Namen des Quell-Mandanten.
1. Wählen Sie im Feld **Quellstandort** den Quellstandort.
1. Wählen Sie **Kopie erstellen**.

> [!NOTE]
> Die Berechtigungen des Mandanten-Administrators sind sowohl für die E-Commerce Umgebung der Quelle als auch des Ziels erforderlich.

Nach der Überprüfung der Informationen zeigt eine Benachrichtigung an, dass ein neuer Auftrag zum Kopieren der Website erstellt wurde. Sie können den Fortschritt des Auftrags im [rechten Fensterbereich der Seite **Mandantenaufträge** überwachen](#monitor-the-site-copy-operation). Wenn der Kopiervorgang erfolgreich abgeschlossen wurde, wird der neue Standort in der Liste der Standorte in der Standortlistenansicht angezeigt.

## <a name="monitor-the-site-copy-operation"></a>Monitor des Vorgangs der Standortkopie

Um den Fortschritt des Vorgangs zum Kopieren der Website zu überwachen, gehen Sie folgendermaßen vor.

1. Melden Sie sich beim Site Builder für die E-Commerce Umgebung des Ziels an.
1. Wählen Sie im linken Fensterbereich **Mandantenaufträge**.
1. Auf der Seite **Aufträge für Mandanten** suchen Sie den Auftrag für die Standortkopie in der Liste und wählen ihn aus. Auf der rechten Seite erscheint ein Fenster mit dem Status und den Details des ausgewählten Auftrags.

Sie können einen Auftrag abbrechen, der den Status **In Bearbeitung** hat. Markieren Sie den Auftrag in der Liste und wählen Sie dann **Abbrechen** im Aktionsbereich.

Sie können einen Auftrag mit dem Status **Fehlgeschlagen** oder **Mit Fehlern abgeschlossen** erneut versuchen. Markieren Sie den Auftrag in der Liste und wählen Sie dann im Aktionsbereich **Wiederaufnahme**.

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
