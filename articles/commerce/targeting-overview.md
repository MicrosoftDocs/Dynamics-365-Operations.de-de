---
title: Adressierung von Geräten, Märkten und Geolocations
description: In diesem Thema wird beschrieben, wie Sie Zielgruppen und Ziele in Microsoft Dynamics 365 Commerce Site Builder mithilfe von Geräte-, Markt- und Geolocation-Informationen erstellen, bearbeiten und verwalten.
author: sushma-rao
ms.date: 02/03/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2021-07-31
ms.dyn365.ops.version: AX 10.0.21
ms.openlocfilehash: 0c8ceb5e59c801e0d3dbc3a57e54c40fa8d967ac
ms.sourcegitcommit: 1eef00796f7c5511f432b01800cdf8920992d7d5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2022
ms.locfileid: "8090693"
---
# <a name="device-market-and-geolocation-targeting"></a>Adressierung von Geräten, Märkten und Geolocations

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Zielgruppen und Ziele in Microsoft Dynamics 365 Commerce Site Builder mithilfe von Geräte-, Markt- und Geolocation-Informationen erstellen, bearbeiten und verwalten.

Dynamics 365 Commerce ermöglicht es Ihnen, Variationen Ihres Seiteninhalts (bekannt als *Ziele*) für bestimmte Kundengruppen (bekannt als *Zielgruppe*) zu personalisieren, um die Bindung und die Zufriedenheit der Benutzer zu steigern. Sie können zuerst entweder eine Zielgruppe oder ein Ziel erstellen. Für eine erfolgreiche Adressierung sind jedoch beide Komponenten erforderlich.

Sie erstellen und verwalten Zielgruppen im Commerce Site Builder basierend auf Kundendaten wie Standort, Geräteinformationen, Anmeldestatus und anderen aus Webanfragen von Kunden dynamisch abgeleiteten Informationen. Sie erstellen und verwalten auch Ziele für E-Commerce-Module und -Fragmente im Commerce Site Builder.

**Haftungsausschluss:** Sie sind dafür verantwortlich, diese Funktion in Übereinstimmung mit allen geltenden Gesetzen und Vorschriften zu verwenden, einschließlich derjenigen, die sich auf die Zielgruppenadressierung und Profilerstellung beziehen. 

## <a name="audiences"></a>Zielgruppen

Eine Zielgruppe ist eine Gruppe von Benutzern, und die Zugehörigkeit zu der Gruppe wird durch eine Reihe dynamischer Regeln bestimmt. Diese Regeln sind einfache Logiktests, die anhand von Informationen ausgeführt werden, die in Kundenanfragen oder anderen verfügbaren Segmenten verfügbar sind. Sie können mehrere Regeln kombinieren, indem Sie UND/ODER-Operatoren verwenden.

Commerce unterstützt systemintern grundlegende Segmente wie Geräteinformationen, Anmeldestatus, Verweiser und Parameter für Abfragezeichenfolgen. Es unterstützt auch erweiterbare Segmente durch Verbindungen zu Drittanbietern.

### <a name="basic-segments"></a>Basissegmente

Standardmäßig sind die folgenden Segmente verfügbar und können in Zielgruppendefinitionen aufgenommen werden:

- **Anmeldungsstatus**: Testen Sie, ob ein Benutzer authentifiziert ist.
- **Geräteplattform**: Testen Sie auf folgende Gerätetypen:

    - Mobiltelefon
    - Schreibtisch
    - Tablet
    - Sonstige

- **Gerätebetriebssystem**: Testen Sie auf folgende Betriebssysteme:

    - Windows
    - Linux
    - iOS
    - Android, sonstige

- **Abfragezeichenfolgenparameter**: Testen Sie, ob ein Schlüssel-Wert-Paar in einem Abfragezeichenfolgenparameter einer Anforderungs-URL vorhanden ist. Zum Beispiel kann für die URL `www.fabrikam.com/en-us/request?promo=true` eine Regel geschrieben werden, um zu testen, dass der Parameter **Promo** den Wert **wahr** hat.
- **Cookie**: Testen Sie auf einen Cookie-Wert, der für die Domäne in der Anforderungs-URL festgelegt ist. Eine Fabrikam.com-Anforderung kann beispielsweise ein Cookie mit dem Namen **Benutzerdefiniertes Layout** und dem Wert **1**. Der Cookie-Test prüft, ob ein Cookie vorhanden ist, erstellt jedoch kein explizites. Im vorherigen Beispiel muss JavaScript zuvor das Cookie für **Benutzerdefiniertes Layout** von einem anderen Modul oder einem anderen Geschäftsprozess festgelegt haben.

    > [!NOTE]
    > Stellen Sie sicher, dass Ihre Verwendung von Cookies den geltenden Gesetzen entspricht.

- **Verweiser**: Wenn ein Benutzer einem Link folgt, um die Seite anzufordern, ist der Verweiser die URL der Seite, die den Link gehostet hat.

### <a name="extensible-segments"></a>Erweiterbare Segmente

Mit Commerce können Sie die Liste der verfügbaren Segmente erweitern, indem Sie eine Verbindung zu Drittanbietern für die Segmentierung herstellen. Ein Segmentierungsanbieter beschreibt die verfügbaren Segmenttypen. Weitere Informationen zum Herstellen einer Verbindung mit einem Geolocation- oder Segmentierungsanbieter finden Sie unter [Connectors konfigurieren und aktivieren](e-commerce-extensibility/connectors.md).

> [!NOTE]
> - Wenn ein externer Anbieter aktiviert ist, stellt er möglicherweise eine Verbindung zu einem Dienst mit unvorhersehbarer Leistung her. Um eine bessere Benutzererfahrung zu gewährleisten, wird die Standardversion der Seite angezeigt, wenn ein Nutzer eine Seite mit Zielgruppenadressierung anfordert und diese Seite auf eine Zielgruppe verweist, die einen Drittanbieter-Segmentanbieter überprüft.
> - Der Benutzer muss zustimmen, um Cookies zuzulassen. Der Browser des Benutzers fordert dann alle Segmente von relevanten Anbietern an und die Ergebnisse werden in einem Cookie abgelegt, das an den Benutzer zurückgegeben wird. Nachfolgende Anfragen an die Seite verwenden diese Informationen, um dem Benutzer zielgerichtete Inhalte bereitzustellen. Weitere Informationen zur Cookie-Compliance finden Sie unter [Cookie-Compliance](cookie-compliance.md).

**Haftungsausschluss:** Wenn Sie diese Funktion aktivieren, werden Ihre Daten an von Ihnen ausgewählte Drittanbietersysteme weitergegeben. Sie kontrollieren, welche Daten Sie gegebenenfalls an Dritteanbeiter weitergeben. Ihnen ist bewusst, dass die Datenverarbeitungs- und Compliance-Standards des Drittanbieters von den Standards von Microsoft Dynamics 365 Commerce abweichen können. Ihre Privatsphäre ist für Microsoft wichtig. Weiteres erfahren Sie in unseren [Datenschutzbestimmungen](https://privacy.microsoft.com/privacystatement).

### <a name="create-an-audience-in-site-builder"></a>Erstellen Sie eine Zielgruppe im Site Builder

Führen Sie die folgenden Schritte aus, um im Commerce Site Builder eine Zielgruppe zu erstellen.

1. Wählen Sie im linken Navigationsbereich die Option **Zielgruppen** aus.
1. Wählen Sie **Neu** aus.
1. Geben Sie einen Namen für die Zielgruppe ein. Optional können Sie auch Tags und eine Beschreibung hinzufügen.
1. Wählen Sie **Erstellen** und dann **Neuen Regelblock hinzufügen** aus. Ein Regelblock ist eine Sammlung von Regeln, die durch UND-Bedingungen verbunden sind. Sie können auch mehrere Regelblöcke erstellen, zwischen denen ODER-Bedingungen bestehen.
1. Wählen Sie eine Datenquelle für Ihre Segmente aus und geben Sie dann den Segmentnamen, den Operator und die Werte an. Sie können in einem Regelblock weitere Regeln erstellen und löschen oder ganze Regelblöcke erstellen und löschen. Sie können auch Regelblöcke nach Bedarf nach oben oder unten verschieben.

    > [!NOTE]
    > Eine Liste kann bis zu 100 Werte enthalten, und jedes Listenelement kann bis zu 50 Zeichen enthalten.

1. Wenn Sie mit der Zielgruppenkonfiguration zufrieden sind, wählen Sie **Bearbeitung beenden**. Sie können dann **Veröffentlichen** auswählen, um das Zielpublikum für die Verwendung in einem Live-Ziel verfügbar machen. Alternativ können Sie die Zielgruppe zusammen mit dem Ziel veröffentlichen. 

Um eine Zielgruppe zu bearbeiten, wählen Sie den Hyperlink dafür auf der Registerkarte **Zielgruppen** und dann **Bearbeiten** im angezeigten Zielgruppen-Editor aus. Um die Liste der Ziele und Seiten anzuzeigen, die auf eine Zielgruppe verweisen, wählen Sie die Zielgruppe in der Zielgruppenlistenansicht und dann **Zuweisungen anzeigen** aus. Um eine Zielgruppe in der Zielgruppenlistenansicht oder im Zielgruppen-Editor zu löschen, heben Sie die Veröffentlichung auf, wenn sie bereits veröffentlicht wurde, und wählen Sie dann **Löschen** in der Befehlsleiste.

> [!NOTE]
> Zielgruppen sind ein Konzept auf Site-Ebene im Commerce Site Builder. Sie können dieselbe Zielgruppe für mehrere Ziele freigeben.

### <a name="rename-an-audience-in-site-builder"></a>Umbenennen einer Zielgruppe in Site Builder

Um eine bestehende Zielgruppe in Commerce umzubenennen, gehen Sie wie folgt vor.

1. Wählen Sie im linken Navigationsbereich die Option **Zielgruppen** aus.
1. Wählen Sie den Namen des Zielgruppensegments, das Sie umbenennen möchten.
1. Wählen Sie **Bearbeiten**, um mit der Bearbeitung der Zielgruppe zu beginnen.
1. Wählen Sie im Bereich Eigenschaften der Zielgruppe das Stiftsymbol neben dem Namen der Zielgruppe.
1. Bearbeiten Sie den Namen der Zielgruppe nach Bedarf.
1. Aktivieren Sie das Kontrollkästchen, um die Namensänderung zu bestätigen.
1. Wählen Sie **Beenden Sie die Bearbeitung**.

## <a name="targets"></a>Ziele

Ein Ziel ist die Benutzererfahrung, die Mitgliedern einer oder mehrerer ausgewählter Zielgruppen gezeigt wird. Es kann Variationen eines oder mehrerer Module auf einer Seite oder in einem Fragment enthalten. 

Sie können einen Zeitplan für Ihre Ziele definieren, um anzugeben, wie lange sie aktiv bleiben sollen. Beachten Sie, dass diese Aktion von der Aktion zum Planen einer Veröffentlichungsgruppe abgetrennt ist, die bestimmt, wann eine Inhaltssammlung veröffentlicht wird. Sie können auch eine Vorschau Ihrer Ziele anzeigen, um zu sehen, wie sie für Mitglieder ausgewählter Zielgruppen aussehen. Darüber hinaus können Sie Ihre Ziele priorisieren, um festzulegen, welches Ziel im Konfliktfall angezeigt werden soll.

### <a name="create-a-target"></a>Ein Ziel erstellen

Führen Sie die folgenden Schritte aus, um im Commerce Site Builder eine Ziel-Shell für Seitenmodule zu erstellen.

1. Wählen Sie im linken Navigationsbereich die Option **Seiten** aus. Wählen Sie dann den Hyperlink für die Seite aus, die die Module enthält, die Sie als Ziel verwenden möchten.
1. Wählen Sie **Bearbeiten** aus, um die Seite zur Bearbeitung zu überprüfen.
1. Wählen Sie im Menü **Ziel** **Neues Ziel** aus, um eine neue Ziel-Shell zu erstellen. Sie können nach Bedarf mehrere Ziele auf einer Seite erstellen.
1. Geben Sie einen Namen und eine neue Beschreibung für Ihr Ziel ein und wählen Sie **Weiter**.
1. Wählen Sie **Hinzufügen** aus, um die Zielgruppen einzuschließen, die den anvisierten Inhalt sehen werden, oder um Zielgruppen auszuschließen. Wählen Sie dann **Weiter** aus.

    > [!NOTE]
    > Die Zielgruppenzuweisung ist ein optionaler Schritt bei der Zielerstellung. Bevor Sie das Ziel veröffentlichen, müssen Sie jedoch mindestens eine Zielgruppe einschließen, um sicherzustellen, dass die beabsichtigten Benutzergruppen den Zielinhalt sehen.

1. Legen Sie das Zeitfenster für die Anzeige Ihres Ziels fest, indem Sie die Zeitzone sowie das Start- und Enddatum und die Uhrzeit auswählen. Sie können das Ziel so einstellen, dass es jederzeit während des Fensters angezeigt wird, oder Sie können bestimmte Tage und Uhrzeiten auswählen. Klicken Sie abschließend auf **Weiter**.

    > [!NOTE]
    > Die von Ihnen angegebenen Zeiten und Zeitzonen sind global. Wenn Sie unterschiedliche Standorte zu unterschiedlichen Zeiten oder in verschiedenen Zeitzonen ansprechen möchten, müssen Sie unterschiedliche Ziele erstellen und für jeden Standort den gewünschten Zeitplan definieren.

1. Überprüfen Sie die Details, und wenn alles richtig aussieht, wählen Sie **Zielumgebung erstellen** und dann **Zum Ziel gehen**. Die Ziel-Shell wird erstellt. Sie können ihr nun Module hinzufügen.
1. Wählen Sie das Zielmodul aus, wählen Sie die Auslassungspunkte (**...**) und dann **Zu aktuellem Ziel hinzufügen** aus. Wenn Sie ein übergeordnetes Modul als Ziel verwenden, werden alle seine untergeordneten Elemente Teil dieses Ziels. Die anvisierten Module sind grün markiert.
1. Nehmen Sie die erforderlichen Inhaltsaktualisierungen am Zielmodul vor, und fügen Sie dem Ziel nach Bedarf weitere Module hinzu. Wählen Sie dann **Speichern** aus, um alle Änderungen zu speichern.
1. Wählen Sie vor der Veröffentlichung Ihres Ziels unbedingt **Vorschau** in der Befehlsleiste, um sie zu überprüfen. Sie können dann eine der folgenden Optionen auswählen:

    - **Einfache Vorschau**: Wählen Sie diese Option aus, um nur die ausgewählte Variante (Standardseite oder Ziel) ohne zugeordnete Zielgruppen in der Vorschau anzuzeigen.
    - **Erweiterte Vorschau**: Wählen Sie diese Option, wenn Sie mehrere Ziele auf einer Seite haben und diese als Benutzer, der zu einer ausgewählten Gruppe von Zielgruppen gehört, oder zu einem bestimmten Datum/Uhrzeit in der Vorschau anzeigen möchten. Wählen Sie **Weiter**, um aus einer Liste relevanter Zielgruppen auszuwählen. Sie können den Filter auch entfernen, um aus allen Zielgruppen auszuwählen.

1. Wenn Sie mit der Zielkonfiguration zufrieden sind, müssen Sie die Seite veröffentlichen, damit das Ziel live geschaltet wird. Wählen Sie **Veröffentlichen** aus, um das Ziel sofort live zu schalten. Alternativ können Sie eine Veröffentlichungsgruppe verwenden, um zu planen, wann die Seite live geht. Weitere Informationen zu Veröffentlichungsgruppen finden Sie unter [Arbeiten mit Veröffentlichungsgruppen](publish-groups.md).

Sie können auch auf Fragmente adressieren. Das Verfahren ist ähnlich. In Schritt 1 wählen Sie jedoch im linken Navigationsbereich **Fragmente** anstatt **Seiten**.

> [!NOTE]
> Um negative Auswirkungen auf Ihre Metriken zu vermeiden, können Sie entweder ein Experiment oder Ziele auf einer Seite oder in einem Fragment verwenden. Sie können nicht sowohl ein Experiment als auch Ziele haben.

### <a name="manage-targets"></a>Ziele verwalten

Um Ziele zu bearbeiten, zu duplizieren oder zu löschen, rufen Sie die Standardseite oder das Fragment auf und führen Sie diese Schritte aus.

1. Wählen Sie im Dropdownmenü **Ziel** und dann **Ziele verwalten** aus.
1. Wählen Sie ein Ziel zum Bearbeiten, Duplizieren oder Löschen aus.
1. Wenn Sie mehrere Ziele im selben Modul haben oder mehrere Ziele widersprüchliche Zeitpläne haben, wählen Sie **Ziele priorisieren** aus, um die Reihenfolge anzugeben, in der sie angezeigt werden sollen. Wenn Sie mehr als ein Ziel auf einer Seite oder in einem Fragment hinzufügen, wird die Schaltfläche **Ziele priorisieren** auch in der Benachrichtigungsleiste angezeigt, um Sie daran zu erinnern, die Ziele zu priorisieren. Wenn keine Priorität angegeben ist, wird standardmäßig das neueste Ziel ausgewählt.

### <a name="localize-targets"></a>Ziele lokalisieren

Ziele auf Seiten und in Fragmenten werden automatisch aufgenommen, wenn XLIFF-Dateien zu Lokalisierungszwecken exportiert und importiert werden. Wenn jedoch keine Gebietsschemas erforderlich sind, können Sie die Ziele dafür löschen, nachdem die lokalisierten XLIFF-Dateien importiert wurden.

> [!NOTE]
> Ziele werden pro Kanal und Gebietsschema verwaltet. Änderungen, die Sie an Zielen in einem Kanal oder Gebietsschema vornehmen, werden nicht automatisch auf andere Kanäle oder Gebietsschemas übertragen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
