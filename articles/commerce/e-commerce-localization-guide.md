---
title: Anleitung für die Dynamics 365 Commerce-E-Commerce-Lokalisierung
description: In diesem Thema wird beschrieben, wie Sie eine Microsoft Dynamics 365 Commerce-E-Commerce-Site in zusätzliche Sprachen lokalisieren und die Site so konfigurieren, dass sie mehrere Kanäle unterstützt.
author: bicyclingfool
ms.date: 04/29/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1e9d91036ceeb9161dc8ee903532b2cf3ca435e2
ms.sourcegitcommit: 26c726bd0b00935e3d2c31fdc5a3b2ae03a8a2b0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661526"
---
# <a name="dynamics-365-commerce-e-commerce-localization-guide"></a>Anleitung für die Dynamics 365 Commerce-E-Commerce-Lokalisierung

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie eine Microsoft Dynamics 365 Commerce-E-Commerce-Site in zusätzliche Sprachen lokalisieren und die Site so konfigurieren, dass sie mehrere Kanäle unterstützt, und behandelt auch die Konzepte und Terminologie im Zusammenhang mit dem Prozess.

Die E-Commerce-Funktionen in Dynamics 365 Commerce wurden entwickelt, um Online-Erlebnisse zu ermöglichen, die auf bestimmte Länder und Sprachen zugeschnitten werden können, aber gleichzeitig die maximale Wiederverwendung von Vorlagen, Seiten, Inhalten und Medien ermöglichen. Sie können auch eine einfache Site erstellen und dann in neue Märkte expandieren, indem Sie im Laufe der Zeit Unterstützung für weitere Länder und Sprachen hinzufügen.

## <a name="definitions"></a>Definitionen

**Gebietsschema, Gebietsschemabezeichner**: Ein Gebietsschema (auch als Gebietsschemabezeichner bezeichnet) definiert eine Sprache, die einem Land oder einer Region zugeordnet ist. Beispielsweise ist der Gebietsschemabezeichner „fr-ca“ dem kanadischen Französisch zugeordnet.

**Ausgangssprache**: Die Sprache, in der Sie Ihre Site-Inhalte entwickeln, bevor Sie sie zur Lokalisierung exportieren.

**Kanal, Onlineshop**: Ein Kanal (auch als Onlineshop bezeichnet) definiert die Zahlungsmethoden, Preisgruppen, Produkthierarchien, Sortimente und Produkte für ein Online-E-Commerce-Schaufenster.

## <a name="concepts"></a>Konzepte

### <a name="url-driven-experience"></a>URL-gesteuerte Erfahrung

Dynamics 365 Commerce-E-Commerce-Sites bieten Kunden einzigartige vermarktete und lokalisierte Erlebnisse über Kanäle und Gebietsschemabezeichner. Kanäle definieren die einzigartigen Produkte, Kategorien, Währungen und Zahlungsmethoden für einen Markt, und Gebietsschemabezeichner bestimmen die Sprache der Inhalte, die Kunden sehen. Eine E-Commerce-Site verwendet URLs, um zwischen vermarkteten und lokalisierten Erfahrungen zu unterscheiden. Site-URLs für diese einzigartigen Kanal- und Gebietsschemaerfahrungen werden für eine Site auf der Seite **Site-Einstellungen \> Kanäle** im Dynamics 365 Commerce Site Builder definiert.

Im Site Builder ist eine URL eine Kombination aus einer Domäne und einem Pfad, die den Einstiegspunkt für eine eindeutige Kombination aus einem Kanal und einem Gebietsschema definiert. Im folgenden Beispiel definiert ein fiktiver Onlineshop namens Fabrikam Inc. vier eindeutige Kombinationen aus einem Kanal und einem Gebietsschema und ordnet jede Kombination einer eindeutigen URL zu, die Kunden Inhalte bereitstellt.

| Domäne                     |  Pfad      | Kanal       |   Gebietsschema     |
|------------------------|--------|--------------------------------|--------|
| `https://fabrikam.com` | /      | Erweiterter Onlineshop von Fabrikam | de  |
| `https://fabrikam.com` | /es    | Erweiterter Onlineshop von Fabrikam | ES     |
| `https://fabrikam.ca`  | /      | Onlineshop von Contoso    | fr-ca  |
| `https://fabrikam.ca`  | /en-ca | Onlineshop von Contoso    | En-ca  |

#### <a name="domain"></a>Domäne

Domains werden eingerichtet, wenn Sie Ihre E-Commerce-Site in Microsoft Dynamics Lifecycle Services (LCS) einrichten. Nachdem Ihre E-Commerce-Umgebung bereitgestellt wurde, können Sie weitere Domains hinzufügen, indem Sie eine Serviceanfrage öffnen. Weitere Informationen darüber, wie Sie Domänen für Ihre E-Commerce-Site einrichten, finden Sie unter [Domänen in Dynamics 365 Commerce](domains-commerce.md).

#### <a name="path"></a>Pfad

- Ein Pfad ist eine beliebige Zeichenfolge, die in Kombination mit der Domäne einer eindeutigen Kombination aus einem Kanal und einem Gebietsschema zugeordnet wird. Im vorherigen Beispiel stimmt die als Pfad verwendete Zeichenfolge mit dem Gebietsschemabezeichner überein, dem der Pfad zugeordnet ist. Sie können jedoch einen anderen Ansatz verwenden.
- Eine Kombination aus Kanal und Gebietsschema kann einer Domäne und einem leeren Pfad („/“) zugeordnet werden. Im vorherigen Beispiel erhalten Kunden, die `https://fabrikam.ca/` besuchen, Produkte und Sortimente für den kanadischen Markt in kanadischem Französisch.
- Commerce Site Builder verhindert, dass Sie doppelte Kombinationen aus einer Domäne und einem Pfad erstellen. Sie können jedoch doppelte Kombinationen aus einem Kanal und einem Gebietsschema einer anderen Kombination aus einer Domäne und einem Pfad zuordnen.

#### <a name="channel"></a>Kanal

- Kanäle (auch als Onlineshops bezeichnet) definieren die Zahlungsmethoden, Preisgruppen, Produkthierarchien, Sortimente und Produkte für ein Online-E-Commerce-Schaufenster.
- Kanäle werden definiert, konfiguriert und veröffentlicht in der Dynamics 365 Commerce-Zentralverwaltung.
- Site Builder kann die Onlineshops erkennen, die in der Commerce-Zentralverwaltung konfiguriert wurden und einer Site zugeordnet werden können.

Weitere Informationen zu Kanälen finden Sie unter [Übersicht über Kanäle](channels-overview.md). Weitere Informationen zur Einrichtung eines Onlinekanals finden Sie unter [Einen Onlinechannel einrichten](channel-setup-online.md).

#### <a name="locale"></a>Gebietsschema

- Das Gebietsschema ist der eigentliche Bezeichner, der verwendet wird, wenn Sie XLIFF-Dateien (XML Localization Interchange File Format) zur Lokalisierung übergeben. Gebietsschemata werden für jeden Kanal in der Commerce-Zentralverwaltung definiert und veröffentlicht. Informationen zum Konfigurieren von Sprachen und Kanälen im Site Builder finden Sie im nächsten Abschnitt.
- Dasselbe Gebietsschema kann mehreren Kanälen zugeordnet werden. Auf diese Weise kann eine gemeinsame Sprache über mehrere Märkte hinweg angeboten werden.

## <a name="configure-languages-and-channels-for-your-e-commerce-site"></a>Sprachen und Kanäle für Ihre E-Commerce-Site konfigurieren

Alle Dynamics 365 Commerce-E-Commerce-Sites sind standardmäßig so konfiguriert, dass sie einen einzigen Onlinekanal und eine einzige Sprache verwenden, unabhängig davon, ob Sie mit der Fabrikam-Demo-Site beginnen oder eine neue Site von Grund auf neu erstellen.

In dieser Konfiguration entwickeln Kunden und Partner in der Regel alle Assets, die länder- und sprachübergreifend verwendet werden. Diese Assets umfassen Vorlagen, Seiten, Fragmente, Inhalt und Medien. Alle Site-Inhalte werden in der ersten Sprache entwickelt, die Sie für Ihre Site ausgewählt haben, oder wenn Sie die Fabrikam-Demo-Site verwenden, werden Site-Inhalte auf Englisch entwickelt.

![Sofort einsatzbereite Dynamics 365 Commerce-E-Commerce-Site](media/loc-guide-1.png)

> [!NOTE]
> Sie können die Fabrikam-Demosite für eine zusätzliche Sprache konfigurieren, sodass die Inhaltsentwicklung in dieser Sprache erfolgen kann. Informationen zum Hinzufügen einer neuen Sprache zu einer Site und einem Kanal finden Sie im Abschnitt [Eine zusätzliche Sprache für Ihre Site konfigurieren](#configure-an-additional-language-for-your-site) weiter unten in diesem Thema.

Das Content-Management-System (CMS) und das Seitenmodell für Dynamics 365 Commerce-E-Commerce-Sites wurden entwickelt, um die Expansion in neue Märkte und Regionen zu ermöglichen. Daher können Sie über eine einzige E-Commerce-Site die Assets für einen Onlineshop verwalten, der mehrere Märkte und Sprachen umfasst.

![Dynamics 365 Commerce-E-Commerce-Site, die mehrere Märkte und Sprachen umfasst](media/loc-guide-2.png)

### <a name="configure-an-additional-language-for-your-site"></a>Eine zusätzliche Sprache für Ihre Site konfigurieren

Der Prozess zum Konfigurieren einer neuen Sprache für eine E-Commerce-Site besteht aus drei Schritten.

#### <a name="step-1-add-the-language-to-your-channel-online-store-in-commerce-headquarters"></a>Schritt 1: Die Sprache zu Ihrem Kanal (Onlineshop) in der Commerce-Zentralverwaltung hinzufügen

1. Gehen Sie in der Commerce-Zentralverwaltung zu dem Kanal, dem Sie die neue Sprache hinzufügen möchten. Wechseln Sie zu **Einzelhandel und Handel \> Kanäle \> Onlineshops**, um die Liste der Kanäle zu finden, die Sie in der Commerce-Zentralverwaltung konfiguriert haben.
1. Öffnen Sie den Onlineshop, der Ihrer Site zugeordnet ist, indem Sie seinen Wert **Retail Channel-Kennung** auswählen. Sie können den Onlineshop, der Ihrer Site zugeordnet ist, überprüfen, indem Sie die **Kanäle**-Site-Einstellungsseite im Commerce Site Builder öffnen und sich den Namen des Onlineshops in der **Kanäle**-Spalte anschauen. 
1. Auf dem Inforegister **Sprachen** wählen Sie **Hinzufügen** aus. Wählen Sie im Feld **Sprache** den Gebietschemacode für die neue Sprache aus. Wählen Sie dann **Speichern** aus.
1. Gehen Sie zu **Einzelhandel und Handel \> IT für Einzelhandel und Handel \> Vertriebsplan**, und führen Sie den Auftrag **1070 Kanalkonfiguration** aus. Wenn die Ausführung des Auftrags abgeschlossen ist, können Sie mit Schritt 2 fortfahren und die Sprache zu einem Kanal für Ihre Site im Site Builder hinzufügen.

![Inforegister „Sprachen“ eines Onlineshops in der Commerce-Zentralverwaltung](media/loc-guide-3.png)

#### <a name="step-2-add-the-language-to-a-channel-in-site-builder"></a>Schritt 2: Sprache zu einem Kanal im Site Builder hinzufügen

Um eine Sprache zu einem Kanal in Site Builder hinzuzufügen, gehen Sie folgendermaßen vor.

1. Öffnen Sie im Commerce Site Builder Ihre Site und öffnen Sie dann die **Kanäle**-Seite in den Site-Einstellungen.
1. Wählen Sie den Namen des Kanals aus, zu dem die Sprache hinzugefügt werden soll.
1. Wählen Sie im rechten Bereich **Gebietsschema hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Gebietsschema hinzufügen** unter **Gebietsschema hinzufügen** das Gebietsschema für die Sprache aus, die Sie zuvor dem Kanal in der Commerce-Zentralverwaltung hinzugefügt haben.
1. Wählen Sie die Domäne und den Pfad aus, die Kunden anfordern, um Ihre Site in diesem Kanal und dieser Sprache anzuzeigen.
1. Wenn Sie möchten, dass die Sprache die Standardsprache zum Anzeigen, Erstellen und Aktualisieren von Site Builder-Seiten und -Fragmenten ist, aktivieren Sie das Kontrollkästchen **Als standardmäßige Kanalsprache für Dokumenterstellung verwenden**. 
    > [!NOTE]
    > Diese Einstellung betrifft nur den Site Builder. Sie hat keinen Einfluss auf die veröffentlichte Site-Erfahrung für Ihre Kunden.
1. Wählen Sie **OK** aus.
1. Wählen Sie **Speichern und veröffentlichen**.

#### <a name="step-3-localize-your-site-content"></a>Schritt 3: Den Inhalt Ihrer Site lokalisieren

Bei Rückkehr in die **Seiten**-Ansicht in Commerce Site Builder wird die neue Sprache in der Kanal- und Gebietsschemaauswahl oben rechts verfügbar sein. Sie können jetzt lokalisierte Versionen von Seiten in Ihrer Ausgangssprache erstellen.

Der Prozess zur Lokalisierung des Inhalts Ihrer Seiten und Fragmente wird im Abschnitt [Inhalte von E-Commerce-Sites lokalisieren](#localize-e-commerce-site-content) weiter unten in diesem Thema behandelt.

### <a name="configure-a-new-channel-for-your-site"></a>Einen neuen Kanal für Ihre Site konfigurieren

Dynamics 365 Commerce-E-Commerce-Sites können Erfahrungen bereitstellen, die über mehrere Onlinekanäle definiert sind, die in der Commerce-Zentralverwaltung konfiguriert werden. Eine Site verwendet mehrere Kanäle, um Kunden eine einzigartige Konfiguration von Zahlungsmethoden, Preisgruppen, Produkthierarchien, Sortimenten und einer Reihe von Produkten zu zeigen. Ein Kanal wird normalerweise verwendet, um diese Dimensionen so zu konfigurieren, dass sie den Anforderungen und Vorlieben für das Erlebnis entsprechen, das mit einzelnen Ländern verbunden ist. Dieser Ansatz ist jedoch eine Geschäftsentscheidung, die der Kunde trifft. Er ist keine Voraussetzung.

Die Voraussetzungen und Aufgaben, die mit der Einrichtung eines Kanals (Onlineshop) verbunden sind, gehen über den Rahmen dieses Dokuments hinaus. Weitere Informationen zur Einrichtung eines Onlinekanals in der Commerce-Zentralverwaltung finden Sie unter [Grundlagen der Kanaleinrichtung](channels-overview.md#channel-setup-basics). Informationen zu den für Onlinekanäle spezifischen Schritten und Anforderungen finden Sie unter [Einen Onlinechannel einrichten](channel-setup-online.md).

Um einen Kanal zu Ihrer Site in Site Builder hinzuzufügen, gehen Sie folgendermaßen vor.

1. Navigieren Sie im Commerce Site Builder zu **Site-Einstellungen \> Kanäle**. 
1. Wählen Sie **Kanal hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Kanal hinzufügen** unter **Kanal** den Kanal aus, den Sie hinzufügen möchten. 
    > [!NOTE]
    > Sie können nur Kanäle hinzufügen, die Ihrer Site noch nicht hinzugefügt wurden.
1. Wählen Sie das Standardgebietsschema für den Kanal aus. Wenn Sie dem Kanal neue Sprachen hinzufügen, können Sie die Standardsprache in eine davon ändern.
1. Geben Sie die Domäne und den Pfad an, die die URL darstellen, die Inhalte und Erfahrungen für diese Kombination aus einem Kanal und einer Sprache bereitstellt.
1. Wählen Sie **OK** aus.
1. Wählen Sie **Speichern und veröffentlichen**.

## <a name="localize-e-commerce-site-content"></a>Inhalte von E-Commerce-Sites lokalisieren

### <a name="xliff-basics"></a>XLIFF-Grundlagen

XLIFF ist ein branchenübliches Dateiformat zum Übergeben lokalisierbarer Inhalte zwischen Content-Management-Tools. Commerce Site Builder verwendet das XLIFF-Dateiformat, um Metadateninhalte von Seiten, Fragmenten und Bildern zu exportieren, damit sie lokalisiert und erneut importiert werden können.

Microsoft Dynamics-Kunden arbeiten in der Regel mit Lokalisierungsanbietern von Drittanbietern wie z. B. [Translated.com](https://translated.com/welcome), um ihre XLIFF-Dateien in die von ihnen benötigten Sprachen zu übersetzen.

### <a name="localize-assets-in-site-builder"></a>Assets im Site Builder lokalisieren

Die folgenden E-Commerce-Site-Assets können im Site Builder lokalisiert werden:

- Seiten
- Fragmente
- Medienobjekte
- Module

Alle neuen Seiten, Fragmente und Medienobjekte werden im Kontext des Kanals und der Sprache erstellt, die derzeit in der Kanal- und Gebietsschemaauswahl ausgewählt sind. Diese Sprache ist normalerweise Ihre „Basissprache“, sofern Sie keine zusätzlichen Sprachen oder Kanäle konfiguriert haben. Auf Sites, auf denen mehrere Kanäle und Sprachen konfiguriert sind, wird die „Basissprache“ durch den Kanal und das Gebietsschema definiert, die Sie als Standard auf der **Kanäle**-Seite in den Site-Einstellungen festgelegt haben.

Die Schritte zum Lokalisieren von Inhalten für Seiten, Fragmente und Medienobjekte sind ähnlich. Auf Ausnahmen und Unterschiede wird in den folgenden Abschnitten hingewiesen. Die Schritte zum Lokalisieren von Modulinhalten unterscheiden sich jedoch. Weitere Informationen finden Sie im Abschnitt [Module lokalisieren](#localize-modules) weiter unten in diesem Thema.

#### <a name="step-1-export-an-xliff-file"></a>Schritt 1: Eine XLIFF-Datei exportieren

Führen Sie die folgenden Schritte aus, um eine XLIFF-Datei für eine Seite, ein Fragment oder ein Bild im Site Builder zu exportieren.

1. Öffnen Sie das Asset, für das Sie Inhalte in der Ausgangssprache exportieren möchten, damit es lokalisiert werden kann.
1. Wählen Sie in der Befehlsleiste **Lokalisierung \> XLIFF exportieren** aus.
    > [!NOTE]
    > Die Option **Lokalisierung** ist nur sichtbar, wenn sich das Asset im Status **Bearbeiten** befindet.

Eine XLIFF-Datei mit dem Namen **\<assetname\>.xlf** wird in den Download-Ordner Ihres Browsers heruntergeladen. Diese XLIFF-Datei ist spezifisch für das Asset, das Sie lokalisieren. Sie exportieren eine XLIFF-Datei für jedes Asset, das Sie lokalisieren möchten.

#### <a name="step-2-localize-the-xliff-file"></a>Schritt 2: XLIFF-Datei lokalisieren

In den meisten Fällen arbeiten Sie mit einem Lokalisierungsanbieter zusammen, um Ihre XLIFF-Dateien zu übersetzen. Wenn Sie jedoch Assets intern lokalisieren oder den Lokalisierungsprozess nur testen möchten, müssen Sie die folgenden Änderungen an einer XLIFF-Datei vornehmen:

- Fügen Sie dem /xliff/file-Element ein Zielsprachenattribut hinzu und setzen Sie den Wert auf den Gebietsschemabezeichner der Sprache, in die Sie lokalisieren. 
    > [!NOTE]
    > Dieser Gebietsschemabezeichner muss mit dem Gebietsschemabezeichner von der **Kanäle**-Seite in den Site-Einstellungen übereinstimmen.
- Fügen Sie für jedes //source-Element ein gleichgeordnetes Zielelement hinzu, wobei der Textwert die lokalisierte Version des Inhalts dieses Quellelements ist.

Informationen zum Schema, das XLIFF-Dateien regelt, finden Sie in der [XLIFF 1.2-Spezifikation](http://docs.oasis-open.org/xliff/xliff-core/xliff-core.html).

> [!NOTE]
> Um ein Asset in mehrere Sprachen zu lokalisieren, müssen Sie für jede dieser Sprachen eine lokalisierte XLIFF-Datei erstellen.

#### <a name="step-3-import-the-localized-xliff-file"></a>Schritt 3: Lokalisierte XLIFF-Datei importieren

Führen Sie die folgenden Schritte aus, um eine XLIFF-Datei für ein Asset zu importieren.

1. Öffnen Sie im Commerce Site Builder das Asset, für das Sie eine XLIFF-Datei importieren möchten.
1. Wählen Sie in der Kanal- und Gebietsschemaauswahl oben rechts den Kanal und die Sprache aus, für die Sie lokalisierte Inhalte importieren.
1. Wählen Sie in der Befehlsleiste **Lokalisierung \> XLIFF importieren** aus. Navigieren Sie dann zur lokalisierten XLIFF-Datei für das ausgewählte Asset und die ausgewählte Sprache und wählen Sie sie aus.

Nachdem die XLIFF-Datei erfolgreich importiert wurde, wird eine „Variante“ der Seite, des Fragments oder Assets erstellt. Ab diesem Punkt wirken sich alle Änderungen, die an der lokalisierten Variante vorgenommen werden, nur auf diese Variante aus. Sie wirken sich nicht auf das Basis-Asset aus, von dem die Variante abgeleitet wurde. Ebenso wirken sich Änderungen am Basis-Asset nicht auf die Variante dieses Assets aus. 

Bei Seiten können Sie jedoch variantenübergreifende Änderungen vornehmen, indem Sie die Vorlage oder das Layout ändern, an die bzw. das diese Seiten gebunden sind. Ebenso wirken sich Änderungen an einem Fragment auf alle Seiten aus, die von dieser Variante abhängig sind.

### <a name="images"></a>Bilder

Bilder können nur dann in einer Seiten- oder Modulvariante gerendert werden, wenn die mit diesen Bildern verknüpften Inhaltsmetadaten lokalisiert sind. Derzeit sind die folgenden Metadaten in einem Medienobjekt lokalisierbar:

- Alternativtext
- Description
- Titel

Derzeit können Sie die Binärdatei für ein digitales Asset wie ein Bild oder ein Video nicht lokalisieren. Das Dynamics 365 Commerce-Produktteam arbeitet derzeit an dieser Funktion.

### <a name="localize-modules"></a>Module lokalisieren

Zeichenfolgen, die als Teil des Moduls selbst gerendert werden (z. B. „Zurück“ und „Weiter“ in einem Karussellmodul), werden getrennt vom Modulinhalt lokalisiert. Anweisungen finden Sie unter [Ein Modul lokalisieren](e-commerce-extensibility/localize-module.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Seitenmodell-Glossar](page-elements-overview.md)

[Kanalübergreifende Freigabe](cross-channel-sharing.md)

[Lokalisieren eines Moduls](e-commerce-extensibility/localize-module.md)

[Moduldefinitionsdatei](e-commerce-extensibility/module-definition-file.md)

[Commerce-Erweiterungsressourcen und Beschriftungsdateien lokalisieren](dev-itpro/extension-resource-localization.md)

[Module mithilfe der CultureInfoFormatter-Klasse globalisieren](e-commerce-extensibility/globalize-modules.md)

[App-Einstellungen: Themen](e-commerce-extensibility/app-settings.md#themes-section)
