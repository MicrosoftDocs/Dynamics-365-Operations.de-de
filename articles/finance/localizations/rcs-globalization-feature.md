---
title: Regulatory Configuration Services (RCS) – Globalisierungsfunktionen
description: In diesem Thema wird erläutert, wie Sie Microsoft Regulatory Configuration Services (RCS) und die das globale nutzen, um die Globalisierungsfunktionen zu erstellen und zu nutzen.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: b701e6bfa14ac30e02bfe79666963db4ee657302
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002787"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a>Regulatory Configuration Services (RCS) – Globalisierungsfunktionen

[!include [banner](../includes/banner.md)]

Mit Microsoft Regulatory Configuration Services (RCS) können Sie eine Globalisierungsfunktion erstellen, die in Globalisierungsdiensten verwendet werden kann, z. B. als E-Invoicing-Service. Mit RCS können Sie folgende Aufgaben ausführen:

- Definieren Sie verwandte Komponenten einer Funktion.
- Verwalten Sie den Lebenszyklusfunktion über den Status einer Funktion.
- Stellen Sie eine Funktion für definierte Umgebungen zur Verfügung.
- Teilen Sie eine Funktion mit anderen Organisationen.

In den folgenden Verfahren wird erläutert, wie ein Benutzer in RCS eine Globalisierungsfunktion und zugehörige Komponenten hinzufügen, den Status der Funktion aktualisieren und die Funktion verfügbar machen kann, damit sie in Globalisierungsdiensten verwendet werden kann.

Bevor Sie die Prozeduren ausführen, müssen Sie die Schritte ausführen, die sich auf die folgenden Aufgaben beziehen:

- Zugriff auf eine RCS-Instanz.
- Konfigurationsanbieter erstellen und aktivieren. Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

In Ihren Finance and Operations Apps Instanzen befolgen Sie diese Schritte.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wenn keine RCS-Umgebung für Ihr Unternehmen bereitgestellt wurde, klicken Sie auf **Regulatory services – Konfiguration** und folgen Sie den Anweisungen zur Bereitstellung einer RCS-Umgebung.

> [!NOTE]
> Wenn für Ihr Unternehmen bereits eine RCS-Umgebung bereitgestellt wurde, verwenden Sie die Seiten-URL, um auf die Umgebung zuzugreifen, indem Sie die Anmeldeoption auswählen.

## <a name="turn-on-the-globalization-features"></a>Aktivieren Sie die Globalisierungsfunktionen

1. Wählen Sie in Ihrer RCS-Instanz die Kachel **Funktionsverwaltung** aus.
2. In dem **Funktionsverwaltung** Arbeitsbereich wählen Sie **Globalisierungsfunktionen** in der Liste und wählen Sie dann **Jetzt aktivieren**.

    ![Globalisierungsfunktionen in der Funktionsverwaltung](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a>Globalisierungsfunktionen

Um eine Globalisierungsfunktion zu verwenden, müssen Sie sie zuerst aus dem globalen Repository importieren und eine eigene Version davon erstellen. Es gibt zwei Möglichkeiten, Globalisierungsfunktionen hinzuzufügen:

- Fügen Sie eine abgeleitete Funktion hinzu, die auf einer vorhandenen Funktion basiert, die veröffentlicht oder freigegeben wurde.
- Fügen Sie eine neue Funktion hinzu, die Sie von Grund auf neu erstellt haben.

## <a name="access-globalization-features"></a>Zugreifen auf Globalisierungsfunktionen

1. Stellen Sie sicher, dass die **Globalisierungsfunktionen** Funktion in der Funktionsverwaltung aktiviert ist wie weiter oben in diesem Thema beschrieben.
2. Öffnen Sie den neuen Arbeitsbereich **Globalisierungsfunktionen** und dann unter **Eigenschaften** wählen Sie die Kachel **elektronische Rechnungsstellung** aus.

    ![Arbeitsbereich für globale Funktionen](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    Die Seite **Funktionen für die elektronische Rechnungsstellung** wird geöffnet.

    ![Seite mit den Funktionen für die elektronische Rechnungsstellung](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a>Fügen Sie eine abgeleitete Globalisierungsfunktion hinzu

Sie können eine neue Globalisierungsfunktion hinzufügen, indem Sie sie von einer vorhandenen Funktion ableiten, die veröffentlicht oder freigegeben wurde.

1. Wählen Sie **Importieren**, um die Seite **Importfunktion aus dem globalen Repository** zu öffnen.

    ![Funktion von der globalen Repository-Seite importieren](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. Wählen Sie **Synchronisieren**, um die neuesten Funktionen zu erhalten.

    Die synchronisierte Liste enthält Funktionen, die Ihnen entweder zur Verfügung stehen, weil sie von Microsoft veröffentlicht wurden oder weil sie von einem anderen Konfigurationsanbieter für Sie freigegeben wurden.

    ![Synchronisierte Liste der Funktionen](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. Wählen Sie in der Liste die zu importierenden Funktionen aus und wählen Sie dann **Importieren**. Sie erhalten eine Nachricht, wenn die ausgewählten Funktionen erfolgreich importiert wurden.

    ![Meldung für erfolgreichen Import](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. Wählen Sie **Hinzufügen** und dann im Dropdown-Dialogfeld die Option **Basierend auf der vorhandenen Version** aus.
5. Geben Sie einen Namen und eine Beschreibung für die Funktion ein.
6. Wählen Sie in der Liste der verfügbaren Funktionen die Basisversion der Funktion aus und wählen Sie dann **Funktion erstellen**.

    ![Hinzufügen einer abgeleiteten Funktion](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    Die von Ihnen hinzugefügte Funktion wird erstellt und hat den Status **Entwurf**.

    ![Abgeleitete Funktion mit Entwurfsstatus](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. Überprüfen Sie die Funktionskomponenten, um festzustellen, ob Aktualisierungen erforderlich sind:

    - Überprüfen Sie die Konfigurationen, falls Sie die ER-Formate (Electronic Reporting) und ihre Bindung mit Formatzuordnungen für die Funktion-Version anpassen müssen.
    - Überprüfen Sie die Einrichtung, falls Sie die Registerkarte **Aktionen**, die Registerkarte **Anwendbarkeitsregeln** oder die Registerkarte **Variablen** für die Funktion-Version anpassen müssen.

8. Auf der Registerkarte **Versionen** wählen Sie **Gültig ab** Datum aus und geben Sie eine Beschreibung ein, wenn das Feld **Beschreibung** leer ist.
9. Wählen Sie **Status ändern**, um die Funktion zu vervollständigen. Abgeschlossene Funktionen können für eine bestimmte Umgebung verfügbar gemacht werden, damit sie in Globalisierungsdiensten verwendet oder im globalen Repository veröffentlicht werden können.

> [!NOTE]
> Funktionen, die einen **Funktionsversionsstatus**-Wert **Veröffentlicht** haben, können mit externen Organisationen geteilt werden.

## <a name="add-a-new-globalization-feature"></a>Fügen Sie eine neue Globalisierungsfunktion hinzu

Sie können eine neue Globalisierungsfunktion hinzufügen, indem Sie sie von Grund auf neu erstellen.

1. Auf der Seite **Importfunktion aus dem globalen Repository** wählen Sie **Hinzufügen** und dann im Dropdown-Dialogfeld die Option **Neue Funktion** aus.
2. Geben Sie einen Namen und eine Beschreibung für die Funktion ein.
3. Wählen Sie **Funktion erstellen**.

    ![Hinzufügen einer neuen Funktion](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. Auf der Registerkarte **Versionen** wählen Sie **Gültig ab** Datum und wählen Sie dann **Status ändern**, um die Funktion zu vervollständigen. Abgeschlossene Funktionen können für eine bestimmte Umgebung verfügbar gemacht werden, damit sie in Globalisierungsdiensten verwendet oder im globalen Repository veröffentlicht werden können.

> [!NOTE]
> Funktionen, die einen **Funktionsversionsstatus**-Wert **Veröffentlicht** haben, können mit externen Organisationen geteilt werden.

## <a name="feature-component-overview"></a>Funktionskomponenten-Übersicht

Globalisierungsfunktionen bestehen aus mehreren Komponenten:

- **Version** – Diese Komponente unterstützt die Verwaltung des Funktionslebenszyklus und ermöglicht Benutzern die Verwaltung des Status für verschiedene Versionen der Funktion.
- **Konfigurationen** – Mit dieser Komponente können Benutzer verwandte ER-Formate und Formatzuordnungen verwalten, anzeigen und bearbeiten.
- **Einrichtungen** – Mit dieser Komponente können Benutzer von Globalisierungsdiensten, z. B. einem E-Invoicing-Dienst, die Einrichtung der zugehörigen Funktionsversion verwalten. Daher unterstützt es die flexible Erstellung von Kommunikations- und Antwortregeln.
- **Umgebung** – Mit dieser Komponente können Benutzer von Globalisierungsdiensten, z. B. einem E-Invoicing-Dienst, die Umgebung verwalten, in der die Einrichtung der Funktions-Version verwendet wird, und den Benutzern, die Zugriff darauf haben, die Berechtigung erteilen.
- **Organisationen** – Mit dieser Komponente können Benutzer die Funktion für externe Organisationen freigeben.

## <a name="configuring-feature-components"></a>Funktionskomponenten konfigurieren

### <a name="version-and-status"></a>Status und Version

Die Version wird zum Verwalten des Lebenszyklus von Globalisierungsfunktionen verwendet.

Der Status kann im Feld **Status** auf der Registerkarte **Ausführung** geändert werden. Folgende Status sind verfügbar:

- **Entwurf** – Die Funktion kann nur bearbeitet werden, wenn sie sich in diesem Status befindet.
- **Abgeschlossen** – Die Funktion und alle zugehörigen Komponenten wurden finalisiert (abgeschlossen) und können nicht bearbeitet werden.
- **Veröffentlicht** – Die Funktion und alle zugehörigen Komponenten wurden im globalen Repository veröffentlicht.
- **Geteilt** – Die Funktion und alle zugehörigen Komponenten wurden an externe Organisationen weitergegeben.
- **Aktiviert** – Die Funktion und alle zugehörigen Komponenten wurden für die Verwendung in einem Globalisierungsdienst aktiviert, z. B. einem E-Invoicing-Dienst.

> [!NOTE]
> Funktionen müssen sich nacheinander durch einige dieser Status bewegen. Daher ist möglicherweise nicht jeder Status in jeder Lebenszyklusphase verfügbar.

### <a name="configurations"></a>Varianten

Die folgenden Aktionen sind für Konfigurationen verfügbar:

- **Anzeigen** – Zeigen Sie die zugrunde liegenden Funktionskonfigurationen an, für die keine Aktualisierung erforderlich ist.
- **Bearbeiten** – Erstellen Sie eine Entwurfsversion einer ausgewählten Konfiguration, damit Sie das Format oder die Formatzuordnung im Format-Designer bearbeiten können.
- **Löschen** – Löschen Sie eine ausgewählte Konfiguration aus der Funktion.
- **Zurücksetzen** – Funktion zurücksetzen. Weitere Informationen finden Sie unter [Zurücksetzen abgeleiteter Glogalisierungsfunktionen](#rebase) weiter unten in diesem Thema.

### <a name="setups"></a>Einrichtungen

Folgende Aktionen sind für die Funktionseinrichtung verfügbar:

- **Hinzufügen** – Erstellen Sie eine neue Funktionseinrichtung. Diese Funktioneinrichtung kann aus einer vorhandenen Funktionseinrichtung abgeleitet oder von Grund auf neu erstellt werden.
- **Löschen** – Löschen Sie eine ausgewählte Funktionseinrichtung.
- **Anzeigen** – Zeigen Sie eine zugrunde liegende Funktionseinrichtung an, für die keine Änderungen erforderlich sind.
- **Bearbeiten** – Erstellen, Löschen oder Ändern der Attribute der drei Hauptkomponenten einer Funktionseinrichtung:

    - Aktionen und ihre Parameter
    - Regeln für die Anwendbarkeit
    - Variable

![Funktionsversion-Einrichtungsseite](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a>Umgebungen

Die folgenden Aktionen sind für Umgebungen verfügbar:

- **Aktivieren** – Wählen Sie für eine ausgewählte Funktions-Version eine veröffentlichte Umgebung und ein **Gültig ab** Datum aus, an dem sie verfügbar sein sollte. Weitere Informationen finden Sie unter [Umgebungen für Aktivieren](#configureenvironment) weiter unten in diesem Thema.
- **Stornieren** – Entfernen Sie eine Umgebung für eine Funktionseinrichtung.

### <a name="organizations"></a>Organisation

Befolgen Sie diese Schritte, um eine Globalisierungsfunktion für eine externe Organisation freizugeben.

1. Auf der **Funktionen für die elektronische Rechnungsstellung** wählen Sie auf dieser Seite die Funktion und die Funktionsversion aus, die Sie freigeben möchten.
2. Auf der **Organisationen** Registerkarte wählen Sie **Teilen mit** und geben Sie dann im Dropdown-Dialogfeld den Domänennamen der Organisation ein.
3. Wählen Sie **Teilen**.

    ![Teilen Sie eine Funktion mit einer Organisation](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

Die Funktion wird für die ausgewählte Organisation freigegeben und steht dieser Organisation im globalen Repository zur Verfügung. Von dort kann die Funktion in die Instanz der Organisation von RCS oder Dynamics 365 Finance importiert werden, damit sie verwendet werden kann.

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a>Zurücksetzen abgeleiteter Globalisierungsfunktionen

Sie können eine zurückgesetzte Globalisierungsfunktion auf die neue oder aktualisierte Version der Basisfunktion zurücksetzen. Auf diese Weise können Änderungen, die in der Basisversion aufgetreten sind, automatisch aktualisiert werden. Die aktualisierte Version der Basisfunktion wird vom ursprünglichen Konfigurationsanbieter erstellt und dann veröffentlicht oder freigegeben.

![Aktualisierte Version der Basisfunktion](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

Wenn Sie beispielsweise die abgeleitete Version einer von Ihnen erstellten Funktion neu erstellen möchten, erhalten Sie zuerst die neueste Version der Funktion, indem Sie sie aus dem globalen Repository importieren.

1. Auf der **Funktionen für die elektronische Rechnungsstellung** Seite wählen Sie **Importieren**.
2. Wählen Sie **Synchronisieren**, um die neuesten Funktionen zu erhalten.
3. Wählen Sie in der Liste der Funktionen die zu importierenden Funktionen aus und wählen Sie dann **Importieren**.

    ![Importieren der neuesten Version einer Funktion](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. Wählen Sie in der Liste der Funktionen die Funktion aus, die neu erstellt werden soll.
5. Auf der Registerkarte **Version** wählen Sie **Neu**, um eine Entwurfsversion zu erstellen.

    ![Neue Entwurfsversion erstellt](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. Wählen Sie **Zurücksetzen**.
7. In dem Dialogfeld **Zurücksetzen** wählen Sie die neueste Version der Funktion aus zum Zurücksetzen.

    ![Dialogfeld zurücksetzen](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. Wählen Sie **OK**.
9. Überprüfen Sie die Funktionskomponenten und nehmen Sie alle notwendigen Änderungen vor.
10. Wählen Sie **Status ändern**, um die Funktion zurückzusetzen. Wenn die Zurücksetzung abgeschlossen ist, können Sie zusätzliche Aktionen ausführen. Sie können die Funktion beispielsweise veröffentlichen und für die Verwendung in Globalisierungsdiensten verfügbar machen.

    ![Funktionsstatus auf Abgeschlossen aktualisiert](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a>Konfigurieren Sie Umgebungen für Globalisierungsfunktionen

Benutzer von Globalisierungsdiensten können die Umgebung verwalten, um eine Globalisierungsfunktion einzurichten und anderen Benutzern, die Zugriff darauf haben, die Berechtigung zu erteilen.

1. Öffnen Sie die Umgebung **Globalisierungsfunktionen** und dann unter **Eigenschaften** wählen Sie die Kachel **elektronische Rechnungsstellung** aus.

    ![Arbeitsbereich für globale Funktionen](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. Wählen **Key Vault-Parameter** und dann **Neu**, um den Azure Key Vault-Schlüssel zu erstellen.
3. Geben Sie einen Namen und eine Beschreibung für das Schlüsseldepot ein und geben dann in das Feld **Key Vault URI** die URL ein, die die Key Vault-Ressource in Azure identifiziert.
4. Auf dem Inforegister **Zertifikate** wählen Sie **Hinzufügen**, um das Zertifikat hinzuzufügen, geben Sie einen Namen und eine Beschreibung für jedes Zertifikat ein.

    ![Zertifikat hinzugefügt](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. Wählen Sie **Neu** aus, um eine neue Umgebung zu erstellen.
6. Geben Sie einen Namen, eine Beschreibung und den für das Speichern erforderliche Signatur-Token-Schlüssel für den gemeinsamen Zugriff ein.
7. Auf dem Inforegister **Benutzer** wählen Sie **Neu**, um einen Benutzer hinzuzufügen, der über die Berechtigung zum Zugriff auf diese Umgebung verfügt.
8. Geben Sie die Benutzer-ID und die E-Mail-Adresse des Benutzers ein.
9. Wiederholen Sie zum Hinzufügen weiterer Benutzer die Schritte 7 und 8.
10. Wählen Sie **Veröffentlichen**, um die Umgebung zu veröffentlichen.

    ![Veröffentlichte Umgebung](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)
