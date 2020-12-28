---
title: Einrichten des Add-Ons für die elektronische Rechnungsstellung
description: In diesem Thema wird erläutert, wie das Add-On für die elektronische Rechnungsstellung in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management eingerichtet wird.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7e631f1bf64b47b5f3e85d4f98c6edafe67d627a
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/19/2020
ms.locfileid: "4443754"
---
# <a name="set-up-the-electronic-invoicing-add-on"></a>Einrichten des Add-Ons für die elektronische Rechnungsstellung

[!include [banner](../includes/banner.md)]


Bei der Einrichtung der Add-On-Funktion für die elektronische Rechnungsstellung wird die erforderliche Konfiguration über die RCS-Umgebung (Regulatory Configuration Services) erstellt und auf dem Add-On-Server für die elektronische Rechnungsstellung veröffentlicht. Mit der Einrichtung können Sie die konfigurierbaren Regeln erstellen, die es dem Add-On für die elektronische Rechnungsstellung ermöglichen, ein sicheres Protokoll über das Internet zu verwenden, um über Webdienste mit einer Drittanbieterentität zu kommunizieren und Daten auszutauschen.

Die Konfigurierbarkeit basiert auf der Konfiguration des Formats der elektronischen Berichterstattung (EB), um Inhalte zu erstellen, die über digitale Dateien gesendet und empfangen werden. Sie basiert auch auf der Orchestrierung von Kommunikationsaktionen, um Anforderungen an Webdienste von Drittanbietern zu senden und Antworten von diesen zu empfangen, ohne dass Sie Code schreiben müssen.

## <a name="overview"></a>Übersicht

„Die Add-On-Funktion für die elektronische Rechnungsstellung“ ist der generische Name für die Ressource, die so konfiguriert und veröffentlicht ist, dass sie den Add-On-Server für die elektronische Rechnungsstellung verwendet. Das Einrichten der Funktion umfasst unter anderem die Verwendung von EB-Konfigurationsformaten zum Erstellen konfigurierbarer Export- und Importdateien sowie die Verwendung von Aktionen und Aktionsabläufen, um die Erstellung konfigurierbarer Regeln zum Senden von Anforderungen, zum Importieren von Antworten und zum Analysieren des Inhalts der Antworten zu ermöglichen.

Die folgende Abbildung zeigt die Hauptkomponenten einer Add-On-Funktion für die elektronische Rechnungsstellung.

![Übersicht über die Add-On-Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-feature-setup-Overview-e-Invoicing-feature.png)

Aufgrund unterschiedlicher Rechnungsformate und Aktivitätsabläufe kann die Einrichtung der Funktionen je nach Land oder Region oder je nach Geschäftsanforderungen variieren.

## <a name="set-up-the-electronic-invoicing-add-on-feature"></a>Einrichten der Add-On-Funktion für die elektronische Rechnungsstellung

Der Einrichtungsprozess muss in Ihrer RCS-Umgebung abgeschlossen sein. Befolgen Sie diese Schritte, um eine neue Add-On-Funktion für die elektronische Rechnungsstellung zu erstellen.

1. Melden Sie sich bei Ihrer RCS-Umgebung an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktionen** im Abschnitt **Funktionen** die Kachel **Add-On für die elektronische Rechnungsstellung** aus.
3. Wählen Sie auf der Seite **Add-On-Funktionen für die elektronische Rechnungsstellung** die Option **Importieren** aus, um die EB-Datenmodellkonfiguration aus dem globalen Repository zu importieren.
4. Wählen Sie **Hinzufügen** aus, um eine Add-On-Funktion für die elektronische Rechnungsstellung zu erstellen. Sie können die Funktion entweder von Grund auf neu erstellen oder aus einer vorhandenen Add-On-Funktion für die elektronische Rechnungsstellung ableiten.

    ![Hinzufügen einer Add-On-Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature.png)

> [!NOTE]
> Wenn Sie eine neue Add-On-Funktion für die elektronische Rechnungsstellung erstellen, hat diese eine Versionsnummer und der Standardstatus ist auf **Entwurf** festgelegt.

### <a name="configurations"></a>Varianten

Konfigurationen enthalten die EB-Formatkonfigurationen, die für Transformationen und zum Erstellen der Dateien erforderlich sind, die während der Kommunikation mit Webdiensten von Drittanbietern ausgetauscht werden. Eine Add-On-Funktion für die elektronische Rechnungsstellung kann so viele EB-Dateiformatkonfigurationen aufweisen, wie erforderlich sind, je nach den vom Webdienstanbieter bereitgestellten technischen Integrationsspezifikation.

Befolgen Sie diese Schritte, um der Add-On-Funktion für die elektronische Rechnungsstellung EB-Formate hinzuzufügen.

1. Wählen Sie auf der Seite **Add-On-Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Konfigurationen** die Option **Hinzufügen** aus, um EB-Dateiformatkonfigurationen für die Add-On-Funktion für die elektronische Rechnungsstellung hinzuzufügen.

    ![Hinzufügen von Konfigurationen für die Add-On-Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Wenn Sie eine Add-On-Funktion für die elektronische Rechnungsstellung von Grund auf neu erstellen, müssen Sie alle EB-Dateiformatkonfigurationen manuell hinzufügen. Wenn Sie eine Add-On-Funktion für die elektronische Rechnungsstellung von einer vorhandenen Funktion ableiten, werden die EB-Dateiformatkonfigurationen automatisch erstellt, da sie von der ursprünglichen Add-On-Funktion für die elektronische Rechnungsstellung geerbt werden.

2. Wählen Sie **Bearbeiten** aus, um die Seite **Formatdesigner** zu öffnen, auf der Sie die Konfiguration des EB-Dateiformats bearbeiten können.

    ![Bearbeiten von Konfigurationen für die Add-On-Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Während Sie das Format bearbeiten, wird der Status der Konfigurationsversion auf **Entwurf** festgelegt.

3. Verwenden Sie die Seite **Formatdesigner**, um die Dateiformatkonfiguration zu bearbeiten. Weitere Informationen finden Sie unter [Erstellen elektronischer Berichterstellungskonfigurationen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Formatdesignerseite](media/e-Invoicing-services-feature-setup-ER-Format-designer.png)

### <a name="feature-setups"></a>Funktionseinrichtungen

Funktionseinrichtungen beinhalten die Regeln für Kommunikation und Sicherheit mit dem Webdienst eines Drittanbieters. Eine Add-On-Funktion für die elektronische Rechnungsstellung kann basierend auf der Geschäftsregel, die Sie umsetzen möchten, so viele Funktionseinrichtungen haben, wie erforderlich sind.

Befolgen Sie diese Schritte, um der Add-On-Funktion für die elektronische Rechnungsstellung Funktionseinrichtungen hinzuzufügen.

1. Wählen Sie auf der Seite **Add-On-Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Einrichtungen** die Option **Hinzufügen** aus, um Funktionseinrichtungen zur Add-On-Funktion für die elektronische Rechnungsstellung hinzuzufügen.

    ![Hinzufügen von Funktionseinrichtungen zur Add-On-Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Setups.png)

    > [!NOTE]
    > Wenn Sie eine Add-On-Funktion für die elektronische Rechnungsstellung von Grund auf neu erstellen, müssen Sie alle erforderlichen Funktionseinrichtungen manuell hinzufügen. Wenn Sie eine Add-On-Funktion für die elektronische Rechnungsstellung von einer vorhandenen Funktion ableiten, werden alle Funktionseinrichtungen automatisch erstellt, da sie von der ursprünglichen Add-On-Funktion für die elektronische Rechnungsstellung geerbt werden.

2. Wählen Sie **Bearbeiten** aus, um die Einrichtung der Funktionsversion zu bearbeiten.

    ![Bearbeiten von Funktionseinrichtungen der Add-On-Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Setups.png)

3. Verwenden Sie die Seite **Einrichtung der Funktionsversion** zum Konfigurieren von Aktionen, Anwendbarkeitsregeln und Variablen.

    ![Aktionen, Anwendbarkeitsregeln und Variablen](media/e-Invoicing-services-feature-setup-View-Actions-Applicability-Rules-Variables.png)

### <a name="actions"></a>Aktionen

Aktionen sind eine vordefinierte Liste von Vorgängen, die in sequenzieller Reihenfolge ausgeführt werden. Diese Liste enthält die Aufschlüsselung der Schritte, die für die vollständige Ausführung der Add-On-Funktion für die elektronische Rechnungsstellung erforderlich sind. Die Aktionen können in derselben Add-On-Funktion für die elektronische Rechnungsstellung die Kommunikation in beide Richtungen umfassen: Senden einer Anforderung für ein Ziel sowie Empfangen einer Antwort und Analysieren Ihres Inhalts.

Jede Aktion enthält eine vordefinierte Liste von Parametern, die erforderlich sind, damit die Aktion ihren Zweck erfüllt. Optional können zusätzliche Parameter bereitgestellt werden.

#### <a name="actions-fasttab"></a>Inforegister „Aktionen“

Führen Sie auf der Seite **Einrichtung der Funktionsversionen** auf der Registerkarte **Aktionen** auf dem Inforegister **Aktionen** einen oder beide der folgenden Schritte aus, um Aktionen zu verwalten:

- Wählen Sie **Neu** oder **Löschen** aus, um neue Aktionen hinzuzufügen oder vorhandene Aktionen zu löschen.
- Wählen Sie **Nach oben** oder **Nach unten** aus, um ausgewählte Aktionen im Raster nach oben oder unten zu verschieben und dadurch die Reihenfolge zu ändern, in der sie ausgeführt werden. Aktionen werden in der Reihenfolge ausgeführt, in der sie im Raster von oben nach unten angezeigt werden.

![Aktionen verwalten](media/e-Invoicing-services-feature-setup-Manage-Actions.png)

In der folgenden Tabelle werden die Felder beschrieben, die auf dem Inforegister **Aktionen** verfügbar sind.

| Feld        | Beschreibung |
|--------------|-------------|
| Vorgang       | Es gibt acht vordefinierte Aktionen.<ul><li><strong>Dokument signieren</strong></li><li><strong>FileStoreActionName</strong></li><li><strong>Umwandeln des Dokuments</strong></li><li><strong>Verarbeiten der Antwort</strong></li><li><strong>Aufrufen des REST-Webdienstes</strong></li><li><strong>Aufrufen des mexikanischen PAC-Dienstes</strong></li><li><strong>Aufrufen des brasilianischen SEFAZ-Dienstes</strong></li><li><strong>Aufrufen des italienischen SDI-Dienstes</strong></li></ul> |
| Aktivitätsname  | Der Name der Aktion und ihre Ausführungsreihenfolge. |
| Beschreibung  | Eine Beschreibung der Aktion ein. |
| Wiederholung aktivieren | Ein aktiviertes Kontrollkästchen zeigt an, dass die Aktion wiederholt werden kann, wenn der vorherige Versuch nicht erfolgreich war. |
| Aktivität wiederholen | Im Falle eines erneuten Versuchs die Aktion, von der aus der erneute Versuch gestartet wird. Der Wiederholungsversuch endet dann mit der aktuellen Aktion (einschließlich Wiederholungsversuch). Für Aktionen mit den Parametern **Minimaler Backoff** und **Maximaler Backoff** geben diese die minimale und die maximale Anzahl von Wiederholungsversuchen an. |

#### <a name="parameters-fasttab"></a>Inforegister „Parameter“

Das Inforegister **Parameter** enthält die Parameter für die Aktion, die auf dem Inforegister **Aktionen** ausgewählt ist.

![Inforegister „Parameter“](media/e-Invoicing-services-feature-setup-View-Actions-Parameters.png)

In der folgenden Tabelle werden die Felder beschrieben, die auf dem Inforegister **Parameter** verfügbar sind.

| Feld       | Beschreibung |
|-------------|-------------|
| Name        | Eine vordefinierte Liste von Parametern. Weitere Informationen finden Sie im Abschnitt [Liste der Parameter nach Aktion](#list-of-parameters-by-action). |
| Beschreibung | Eine Beschreibung des Parameters. |
| Wert       | Der Wert des Parameters. |

#### <a name="list-of-parameters-by-action"></a>Liste der Parameter nach Aktion

Die verfügbaren Parameter variieren je nach der Aktion, die auf dem Inforegister **Aktionen** ausgewählt ist.

###### <a name="action-sign-document"></a>Aktion: Dokument signieren

| Parameter                             | Beschreibung |
|---------------------------------------|-------------|
| Eingabedatei                            | Die eingegebene XML-Dokumentdatei, die mit einer elektronischen Signatur signiert werden muss. |
| Zertifikatname                      | Der Name des gespeicherten Zertifikats. |
| Signaturtyp                        | Der Typ der zu verwendenden Signatur. |
| Name der Signaturmethode                 | Der Name der Signaturmethode, mit der eine elektronische Signatur generiert wird. |
| Name der Digest-Methode                    | Die Digest-Methode, mit der eine Digest-Zeichenfolge in der digitalen Signatur generiert wird. |
| Name der Kanonisierungsmethode          | Die Kanonisierungsmethode, die zur Berechnung des Signatur-Hash verwendet wird. |
| Name des Referenzattributs              | Der Attributname, der angibt, wo die Referenz-ID in das Signaturelement eingefügt werden soll. |
| Name des zu signierenden Elements               | Der Name des XML-Elements im Dokument, das mit einer elektronischen Signatur signiert werden muss. Wenn kein Element angegeben ist, wird der Dokumentenstamm signiert. |
| Name des Elements, in das die Signatur eingefügt werden soll   | Der Name des XML-Elements, in das eine generierte digitale Signatur eingefügt werden soll. Wenn kein Element angegeben ist, wird die Signatur in den Dokumentenstamm eingefügt. |
| XLST-Datei mit Digest-Transformation       | Die XSLT-Datei (Extensible Stylesheet Language Transformations), die Digest-Transformationsregeln zum Generieren der Digest-Zeichenfolge für eine elektronische Signatur enthält. |
| Pfad zum Einfügen der Digest-Zeichenfolge          | Der Pfad im Format **\<elementName\>.\<Attribute.Path\>** des Speicherorts, an dem die generierte Digest-Zeichenfolge eingefügt werden muss. |
| Speicherort der Zertifikatnummer           | Der Name des Elements und Attributs, an dem die Zertifikatsnummer abgelegt werden soll. |
| Speicherort der Zertifikatdaten          | Der Name des Elements und Attributs, an dem die Zertifikatdaten (base64) eingefügt werden müssen. |
| Zertifikatnummer im ASCII-Format | Ein Wert, der angibt, ob die Nummer des Zertifikats im ASCII-Format codiert ist. |

###### <a name="action-filestoreactionname"></a>Aktion: FileStoreActionName

| Parameter  | Beschreibung |
|------------|-------------|
| Eingabedatei | Die zu speichernde Eingabedatei. |

###### <a name="action-transform-document"></a>Aktion: Transformieren des Dokuments

| Parameter                       | Beschreibung |
|---------------------------------|-------------|
| Eingabedatei                      | Die Quelldatei, die die Daten bereitstellt, die für die Aktion ausgeführt werden müssen. |
| Planungsrichtung                       | Ein Wert, der angibt, ob das Importformat oder das Exportformat verwendet werden soll. |
| Konfigurationskennung                | Das Format, das ausgeführt werden soll. |
| Konfigurationsversion           | Wenn keine Konfigurationsversion angegeben ist, wird die neueste Version verwendet. |
| Integrationspunkt der Konfiguration | Die Quelldatei, die Daten für die Berichtslaufzeit bereitstellt. |

###### <a name="action-process-response"></a>Aktion: Verarbeiten der Antwort

| Parameter                    | Beschreibung |
|------------------------------|-------------|
| Eingabedatei                   | Die zu analysierende Antwort. |
| Berichtskonfigurationsliste | Eine Liste von Konfigurationen, mit denen Antworten analysiert werden. |

###### <a name="action-call-rest-web-service"></a>Aktion: Aufrufen des REST-Webdienstes

| Parameter                   | Beschreibung |
|-----------------------------|-------------|
| Webdienst-URL             | Die URL, an die Anforderungen gesendet werden sollen. |
| Lautzeitüberschreitung der Webanforderung         | Die maximale Zeit (in Millisekunden), die auf eine Antwort des Webdienstes gewartet wird. |
| Vorgangstyp anfordern      | Der Typ der HTTP-Anforderungsoperation (z. B. **GET**, **POST** oder **DELETE**). |
| Zertifikatnamen           | Die Zertifikatnamen. |
| Codierung des Antwortkörpers      | Die erwartete Codierung des HTTP-Antwortkörpers, damit dieser korrekt decodiert werden kann. |
| Inhaltstyp der HTTP-Anforderung   | Die Header-Eingabe zum Inhaltstyp für HTTP-Anforderungen. |
| Inhaltskörper der HTTP-Anforderung   | Der HTTP-Anforderungstext. (Der Körper kann leer sein.) |
| Abfragewerte für HTTP-Parameter | Parameterabfragewerte, mit denen die URL mit variablen Parametern gefüllt wird. |
| Anforderungsroute               | Der Routenpfad für die HTTP-Anforderung. Die variablen Parameter können in der Notation **\{paramName\}** geschrieben werden. Ein Beispiel: **"api/{id}/submit"**. |
| Routenparameterliste        | Die Routenparameter in Schlüsselwertnotation, mit denen Variablen in die Route eingefügt werden. |
| Benutzerdefinierte HTTP-Header         | Die benutzerdefinierten HTTP-Header, die in die Anforderung eingefügt werden sollen. |
| HTTP-Anforderungscookies        | Eine Liste von Cookies in Schlüsselwertnotation, die in die HTTP-Cookie-Header-Anforderung eingefügt werden sollen. |
| Sicherheitsprotokoll           | Das Sicherheitsprotokoll, das für HTTP-Anforderungen zur Kommunikation mit dem Server verwendet werden soll. (Standardmäßig wird Transport Layer Security \[TLS\] 1.2 verwendet.) |

###### <a name="action-call-mexican-pac-service"></a>Aktion: Aufrufen des mexikanischen PAC-Dienstes

| Parameter                | Beschreibung |
|--------------------------|-------------|
| Eingabedatei               | Die Datei, die XML-Daten enthält, die als Methodeneingabeparameter an den Webdienst gesendet werden. |
| URL-Adresse              | Die Webdienstadresse (Endpunkt). |
| Name der Webmethode (Aktion) | Der Name der Webmethode (Aktion), die ausgeführt werden muss. |
| Bescheinigungen             | Die Zertifikatkette, die für die Clientauthentifizierung durch den Webdienst erforderlich ist. Das Clientzertifikat sollte das letzte Zertifikat in der Kette sein. Die Stamm- und Zwischenzertifikate sollten an erster Stelle stehen. |
| Lautzeitüberschreitung der Webanforderung      | Die maximale Zeit (in Millisekunden), die auf eine Antwort des Webdienstes gewartet wird. |
| Wiederholungsintervall           | Das Intervall zwischen den Versuchen, eine Antwort vom Webdienst abzurufen und zu empfangen. Wenn kein Intervall angegeben ist, werden keine weiteren Wiederholungsversuche durchgeführt, nachdem der erste Aufruf nicht erfolgreich war. |
| Anzahl von Wiederholungen              | Die maximale Anzahl von Wiederholungsversuchen zum Aufrufen und Abrufen einer Antwort vom Webdienst. |
| Wiederholen bis               | Die maximale Zeit (in Millisekunden), in der Wiederholungsaufrufe fortgesetzt werden können. |
| Minimaler Backoff         | Die minimale Backoff-Rate für die exponentielle Berechnung von Wiederholungsintervallen. |
| Maximaler Backoff         | Die maximale Backoff-Rate für die exponentielle Berechnung von Wiederholungsintervallen. |
| Sicherheitsprotokoll        | Das Sicherheitsprotokoll, das für HTTP-Anforderungen zur Kommunikation mit dem Server verwendet werden soll. (Standardmäßig wird TLS 1.2 verwendet.) |

###### <a name="action-call-brazilian-sefaz-service"></a>Aktion: Aufrufen des brasilianischen SEFAZ-Dienstes

| Parameter                | Beschreibung |
|--------------------------|-------------|
| Eingabedatei               | Die Datei, die XML-Daten enthält, die als Methodeneingabeparameter an den Webdienst gesendet werden. |
| URL-Adresse              | Die Webdienstadresse (Endpunkt). |
| Name der Webmethode (Aktion) | Der Name der Webmethode (Aktion), die ausgeführt werden muss. |
| Bescheinigungen             | Die Zertifikatkette, die für die Clientauthentifizierung durch den Webdienst erforderlich ist. Das Clientzertifikat sollte das letzte Zertifikat in der Kette sein. Die Stamm- und Zwischenzertifikate sollten an erster Stelle stehen. |
| Lautzeitüberschreitung der Webanforderung      | Die maximale Zeit (in Millisekunden), die auf eine Antwort des Webdienstes gewartet wird. |
| Wiederholungsintervall           | Das Intervall zwischen den Versuchen, eine Antwort vom Webdienst abzurufen und zu empfangen. Wenn kein Intervall angegeben ist, werden keine weiteren Wiederholungsversuche durchgeführt, nachdem der erste Aufruf nicht erfolgreich war. |
| Anzahl von Wiederholungen              | Die maximale Anzahl von Wiederholungsversuchen zum Aufrufen und Abrufen einer Antwort vom Webdienst. |
| Wiederholen bis               | Die maximale Zeit (in Millisekunden), in der Wiederholungsaufrufe fortgesetzt werden können. |
| Minimaler Backoff         | Die minimale Backoff-Rate für die exponentielle Berechnung von Wiederholungsintervallen. |
| Maximaler Backoff         | Die maximale Backoff-Rate für die exponentielle Berechnung von Wiederholungsintervallen. |
| Sicherheitsprotokoll        | Das Sicherheitsprotokoll, das für HTTP-Anforderungen zur Kommunikation mit dem Server verwendet werden soll. (Standardmäßig wird TLS 1.2 verwendet.) |

###### <a name="action-call-italian-sdi-service"></a>Aktion: Aufrufen des italienischen SDI-Dienstes

| Parameter                | Beschreibung |
|--------------------------|-------------|
| Eingabedatei               | Die Datei, die XML-Daten enthält, die als Methodeneingabeparameter an den Webdienst gesendet werden. |
| URL-Adresse              | Die Webdienstadresse (Endpunkt). |
| Name der Webmethode (Aktion) | Der Name der Webmethode (Aktion), die ausgeführt werden muss. |
| Bescheinigungen             | Die Zertifikatkette, die für die Clientauthentifizierung durch den Webdienst erforderlich ist. Das Clientzertifikat sollte das letzte Zertifikat in der Kette sein. Die Stamm- und Zwischenzertifikate sollten an erster Stelle stehen. |
| Lautzeitüberschreitung der Webanforderung      | Die maximale Zeit (in Millisekunden), die auf eine Antwort des Webdienstes gewartet wird. |
| Wiederholungsintervall           | Das Intervall zwischen den Versuchen, eine Antwort vom Webdienst abzurufen und zu empfangen. Wenn kein Intervall angegeben ist, werden keine weiteren Wiederholungsversuche durchgeführt, nachdem der erste Aufruf nicht erfolgreich war. |
| Anzahl von Wiederholungen              | Die maximale Anzahl von Wiederholungsversuchen zum Aufrufen und Abrufen einer Antwort vom Webdienst. |
| Wiederholen bis               | Die maximale Zeit (in Millisekunden), in der Wiederholungsaufrufe fortgesetzt werden können. |
| Minimaler Backoff         | Die minimale Backoff-Rate für die exponentielle Berechnung von Wiederholungsintervallen. |
| Maximaler Backoff         | Die maximale Backoff-Rate für die exponentielle Berechnung von Wiederholungsintervallen. |
| Sicherheitsprotokoll        | Das Sicherheitsprotokoll, das für HTTP-Anforderungen zur Kommunikation mit dem Server verwendet werden soll. (Standardmäßig wird TLS 1.2 verwendet.) |

### <a name="applicability-rules"></a>Regeln für die Anwendbarkeit

Mit den Anwendbarkeitsregeln können Sie logische Regeln erstellen, die den Nutzungskontext für die Funktionseinrichtung bestimmen. Die Übereinstimmung zwischen dem Kontext des Geschäftsdokuments, das zur Verarbeitung gesendet wird, und den Kriterien für die Anwendbarkeitsregel bestimmt somit, welche Add-On-Funktion für die elektronische Rechnungsstellung zur Verarbeitung dieser Übermittlung verwendet wird.

#### <a name="set-up-applicability-rules"></a>Einrichten von Anwendbarkeitsregeln

1. Wählen Sie auf der Seite **Einrichtung der Funktionsversion** auf der Registerkarte **Anwendbarkeitsregeln** die Option **Neu** aus, um eine Anwendbarkeitsregel hinzuzufügen.

    ![Verwalten von Anwendbarkeitsregeln](media/e-Invoicing-services-feature-setup-Manage-Actions-Applicability-rules.png)

2. Wählen Sie im Raster die Klauseln aus, die gruppiert werden sollen.
3. Wählen Sie **Klausel gruppieren** aus.

    ![Gruppierung von Klauseln](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-clause.png)

    Wenn Klauseln gruppiert werden, wird dem Raster eine neue Spalte hinzugefügt. Diese Spalte gibt den logischen Operator für die gruppierten Klauseln an.

    ![Logischer Operator für gruppierte Klauseln](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-criterias.png)

Um die Gruppierung von Klauseln aufzuheben, wählen Sie die gruppierten Klauseln aus, für die die Gruppierung aufgehoben werden soll, und wählen Sie dann **Gruppierung für Klausel aufheben**.

![Gruppierung für Klauseln aufheben](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-UnGroup-criterias.png)

> [!NOTE]
> Wenn Sie die Gruppierung für eine Klausel aufheben, beginnen Sie immer mit der innersten Gruppierungsebene.

In der folgenden Tabelle werden die Felder beschrieben, die auf der Registerkarte **Anwendbarkeitsregeln** verfügbar sind.

| Feld         | Beschreibung |
|---------------|-------------|
| Und/oder        | Der logische Operator. |
| Feld         | Das Feld, das zum Erstellen der Regel verwendet werden soll. |
| Operatortyp | Der Typ des Operators:<ul><li>Gleich</li><li>Ungleich</li><li>Größer als, kleiner als</li><li>Größer als oder gleich, kleiner als oder gleich</li><li>Enthält</li><li>Beginnen mit</li></ul> |
| Wert         | Das Kriterium für die Regel. |

### <a name="variables"></a>Variable

Sie können Variablen erstellen und diese dann als Eingabewert für einen Parameter einer bestimmten Aktion verwenden. Sie können sie auch verwenden, um zwischen den Add-On-Diensten für die elektronische Rechnungsstellung und dem Client Informationen auszutauschen, die das Ergebnis der Ausführung einer bestimmten Aktion als Teil des Übermittlungs-Flows sind.

#### <a name="set-up-variables"></a>Variablen einrichten

- Wählen Sie auf der Seite **Einrichtung der Funktionsversion** auf der Registerkarte **Variablen** entweder **Neu** oder **Löschen** aus, um Variablen zu verwalten.

    ![Verwalten von Variablen](media/e-Invoicing-services-feature-setup-Manage-Variables.png)

In der folgenden Tabelle werden die Felder beschrieben, die auf der Registerkarte **Variablen** verfügbar sind.

| Feld       | Beschreibung |
|-------------|-------------|
| Name        | Der Name der Variablen. |
| Beschreibung | Eine kurze Beschreibung der Variable. |
| Typ        | Der Typ der Variable:<ul><li><strong>Konstante</strong> – Der Inhalt der Variablen ist fest.</li><li><strong>Vom Client</strong> – Der Inhalt der Variablen wird vom Microsoft Dynamics 365-Client während der Ausführung des Übermittlungsprozesses erfasst.</li><li><strong>An Client</strong> – Der Inhalt der Variablen wird dem Microsoft Dynamics 365-Client während der Ausführung des Übermittlungsprozesses zum Import zur Verfügung gestellt.</li></ul> |
| Datentyp   | Der Datentyp der Variablen:<ul><li>Aktiv</li><li>Datum</li><li>Anzahl</li><li>UUID</li><li>Zeichenfolge</li><li>Datei</li></ul> |
| Wert       | Der Wert der Variablen oder der Name der Aktion, die den Wert der Variablen festlegt. |

### <a name="validate-the-feature-setup"></a>Überprüfen der Funktionseinrichtung

- Wählen Sie auf der Seite **Einrichtung der Funktionsversion** im Aktivitätsbereich die Option **Überprüfen** aus, um die Einrichtung der Funktionsversion zu überprüfen.

   ![Auswählen der Schaltfläche „Überprüfen“](media/e-Invoicing-services-feature-setup-Select-Validate-Button.png)

Die Validierung überprüft die Konsistenz der gesamten Konfiguration. Wenn beispielsweise ein bestimmter Parameter für eine Aktion obligatorisch ist, sein Wert jedoch leer bleibt, erkennt die Validierung diese Inkonsistenz und Sie erhalten eine Warnung.

## <a name="environments"></a>Umgebungen

Eine Add-On-Umgebung für die elektronische Rechnungsstellung muss der Add-On-Funktion für die elektronische Rechnungsstellung zugeordnet und für diese aktiviert sein. Add-On-Umgebungen für die elektronische Rechnungsstellung müssen im Voraus erstellt und veröffentlicht werden, indem die Globalisierungsfunktionen im RCS-Konto Ihres Unternehmens konfiguriert werden.

Befolgen Sie diese Schritte, um eine Add-On-Umgebung für die elektronische Rechnungsstellung für die Add-On-Funktion für die elektronische Rechnungsstellung zu aktivieren.

1. Wählen Sie auf der Seite **Add-On-Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Umgebungen** die Option **Aktivieren** aus, um eine Add-On-Umgebung für die elektronische Rechnungsstellung hinzuzufügen.
2. Wählen Sie im Feld **Gültig ab** das Datum aus, an dem die neue Umgebung wirksam wird.

![Aktivieren einer Add-On-Umgebung für die elektronische Rechnungsstellung](media/e-Invoicing-services-feature-setup-Select-Enable-e-Invoicing-feature-Environment.png)

## <a name="organizations"></a>Organisation

Die Add-On-Funktion für die elektronische Rechnungsstellung kann von mehreren Organisationen gemeinsam genutzt werden.

- Wählen Sie auf der Seite **Add-On-Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Organisationen** die Option **Teilen mit** aus, um die Organisation hinzuzufügen, mit der Sie die Add-On-Funktion für die elektronische Rechnungsstellung teilen möchten.

Wählen Sie **Freigabe aufheben** aus, um die Freigabe der Add-On-Funktion für die elektronische Rechnungsstellung für die Organisation zu beenden.

## <a name="versions"></a>Versionen

Mit Versionen können Sie den Lebenszyklus der Add-On-Funktion für die elektronische Rechnungsstellung steuern, indem Sie ihren Status verwalten. Sie können eine neue Version einer vorhandenen Add-On-Funktion für die elektronische Rechnungsstellung erstellen. Alternativ können Sie, wenn die gesamte Konfiguration für die Add-On-Funktion für die elektronische Rechnungsstellung abgeschlossen ist, den Status der Funktion in **Abgeschlossen** und dann in **Veröffentlichen** ändern.

### <a name="create-a-new-version-of-an-existing-electronic-invoicing-add-on-feature"></a>Erstellen einer neuen Version einer vorhandenen Add-On-Funktion für die elektronische Rechnungsstellung

1. Wählen Sie auf der Seite **Add-On-Funktionen für die elektronische Rechnungsstellung** im Raster auf der linken Seite die Add-On-Funktion für die elektronische Rechnungsstellung aus.
2. Wählen Sie auf der Registerkarte **Versionen** die Option **Neu** aus, um eine neue Version der Add-On-Funktion für die elektronische Rechnungsstellung hinzuzufügen.

### <a name="change-the-status-of-the-electronic-invoicing-add-on-feature"></a>Ändern des Status der Add-On-Funktion für die elektronische Rechnungsstellung

Befolgen Sie diese Schritte, um den Lebenszyklus der Add-On-Funktion für die elektronische Rechnungsstellung zu verwalten.

1. Wählen Sie auf der Seite **Add-On-Funktionen für die elektronische Rechnungsstellung** im Raster auf der linken Seite die Add-On-Funktion für die elektronische Rechnungsstellung aus.
2. Wählen Sie auf der Registerkarte **Versionen** die Option **Status ändern** aus und ändern Sie dann den Status von **Entwurf** zu **Abgeschlossen**.
3. Sie werden aufgefordert, zu bestätigen, dass Sie die Add-On-Funktion für die elektronische Rechnungsstellung und alle ihre Komponenten abschließen möchten. Wählen Sie **Ja** aus, um die Aktion zu bestätigen, oder **Nein** um sie abzubrechen.

    > [!NOTE]
    > Wenn Sie **Ja** auswählen, wird der Status von Konfigurationsversionen, die Bestandteile der Add-On-Funktion für die elektronische Rechnungsstellung sind, automatisch von **Entwurf** zu **Abgeschlossen** geändert.

4. Wählen Sie **Status ändern** aus und ändern Sie dann den Status von **Abgeschlossen** zu **Veröffentlichen**.
5. Sie werden aufgefordert, zu bestätigen, dass Sie die Add-On-Funktion für die elektronische Rechnungsstellung und alle ihre Komponenten im globalen Repository veröffentlichen möchten. Wählen Sie **Ja** aus, um die Aktion zu bestätigen, oder **Nein** um sie abzubrechen.

    > [!NOTE]
    > Wenn Sie **Ja** auswählen, wird der Status von Konfigurationsversionen automatisch von **Abgeschlossen** zu **Freigegeben** geändert.
