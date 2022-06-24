---
title: Kanäle E-Commerce-Websites zuordnen
description: In diesem Artikel werden einige der häufigeren Kanalzuordnungsszenarien in Microsoft Dynamics 365 Commerce beschrieben, die für die meisten anderen Geschäftsanforderungen extrapoliert werden können.
author: samjarawan
ms.date: 05/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 94c43df26e8d6e55a5b6d459b65066d5873e1063
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902762"
---
# <a name="map-channels-to-e-commerce-sites"></a>Kanäle E-Commerce-Websites zuordnen

In diesem Artikel werden einige der häufigeren Kanalzuordnungsszenarien in Microsoft Dynamics 365 Commerce beschrieben, die für die meisten anderen Geschäftsanforderungen extrapoliert werden können.

Dynamics 365 Commerce unterstützt viele Geschäftsszenarien für das Mapping von [Online-Kanälen](#channels), die einen konfigurierten Satz von Produkten, Preisen und Rabatten für [E-Commerce-Website](#e-commerce-sites)-Erlebnisse für Kunden haben.

Dieser Artikel deckt die folgenden Szenarien ab:

- **Ein einsprachiger Kanal, der eine einzige E-Commerce-Website-Erfahrung bietet.** Dieses Szenario könnte beispielsweise eine Website einer einzelnen Marke umfassen, die für den US-amerikanischen Markt konfiguriert ist.
- **Ein mehrsprachiger Kanal, der eine einzige lokalisierte Website-Erfahrung bietet.** Dieses Szenario könnte beispielsweise eine Website einer einzelnen Marke umfassen, die mit französischer und englischer Sprachunterstützung für Kanada konfiguriert ist. In diesem Szenario haben Benutzer, die unterschiedliche Sprachen auswählen, dieselbe Website-Erfahrung, die jedoch in die ausgewählte Sprache jedes Benutzers lokalisiert ist.
- **Ein mehrsprachiger Kanal, der eine andere Website-Erfahrung pro Sprache bietet.** Dieses Szenario könnte beispielsweise eine Website einer einzelnen Marke umfassen, die mit französischer und englischer Sprachunterstützung für Kanada konfiguriert ist. In diesem Szenario gibt es für jede Sprache ein einzigartiges Website-Erlebnis.
- **Mehrere Kanäle (einsprachig und/oder mehrsprachig), die eine einzige lokalisierte Website-Erfahrung haben.** Dieses Szenario könnte beispielsweise eine Website einer einzelnen Marke umfassen, die für Australien und Neuseeland konfiguriert ist. In diesem Szenario haben beide Länder die gleiche Website-Erfahrung auf Englisch, aber jedes Land ist mit unterschiedlichen Produkten, Währungen, Preisen, Rabatten und Versandarten konfiguriert.
- **Mehrere Kanäle (einsprachig und/oder mehrsprachig), die eine einzige andere Website-Erfahrung pro Kanal haben.** Dieses Szenario könnte beispielsweise eine Website einer einzelnen Marke umfassen, die in mehreren Sprachen für Australien, Kanada und Deutschland konfiguriert ist. In diesem Szenario hat jedes Land eine einzigartige Website-Erfahrung, die mit unterschiedlichen Produkten, Währungen, Preisen, Rabatten und Versandarten konfiguriert ist.

## <a name="channels"></a>Kanäle

Ein Kanal (auch als Online-Shop oder Onlinekanal bezeichnet) stellt ein Online-E-Commerce-Schaufenster dar, das verwendet wird, um Produkte, Preise, Rabatte, Sprachen, Zahlungsmethoden, Liefermodi, Auftragserfüllungs-Zentren und andere Aspekte des Online-Erlebnisses abzubilden, die Ihren E-Commerce-Kunden zur Verfügung stehen. Kanäle werden in Commerce headquarters erstellt und verwaltet und einer einzigen [juristischen Person](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json#legal-entities) zugeordnet. Die juristische Person hat normalerweise ihren Sitz in einem einzigen Land, das eine Steuererklärung für den Kanal erfordert, und mit nur einer einzigen Währung konfiguriert werden kann.

Weitere Informationen zu Kanälen finden Sie unter [Kanalübersicht](channels-overview.md). Weitere Informationen zur Erstellung eines Onlinekanals finden Sie unter [Einen Onlinechannel einrichten](channel-setup-online.md).

Die folgende Beispielabbildung aus Commerce headquarters zeigt die standardmäßigen Onlinekanäle, die mit Dynamics 365 Commerce bereitgestellt werden, wenn die Option für Demodaten ausgewählt ist.

![Standard-Demodatenkanäle in Commerce headquarters.](media/channel-mapping-1.png)

## <a name="e-commerce-sites"></a>E-Commerce-Websites

Eine E-Commerce-Website enthält eine Reihe von Website-Seiten, die Kunden zum Durchsuchen und Einkaufen verwenden. E-Commerce-Websites werden im Commerce-Website-Generator verwaltet.

Weitere Informationen zum Erstellen und Verwalten von Websites im Website-Generator finden Sie unter [Übersicht über E-Commerce-Websites](online-store-overview.md).

## <a name="common-channel-mapping-scenarios"></a>Gängige Kanal-Mapping-Szenarien

Dynamics 365 Commerce unterstützt eine breite Palette von Kanal-Mapping-Szenarien. Die folgenden Kanal-Mapping-Szenarien sind nur eine Teilmenge aller möglichen Kanal-Mapping-Szenarien. Sie sind als Anleitung gedacht, um Ihnen bei der Planung Ihrer einzigartigen Geschäftsszenarien zu helfen. Das fiktive Sportgeschäft Adventure Works, das in den Dynamics 365 Commerce-Demodaten enthalten ist, wird als Beispiel für jedes Szenario verwendet.

### <a name="single-language-channel-that-has-a-single-e-commerce-site-experience"></a>Ein einsprachiger Kanal, der eine einzige E-Commerce-Website-Erfahrung bietet

Im einfachsten Szenario hat ein einzelner Kanal eine einzige Sprache für den Verkauf auf einem einzigen Markt. Ein Beispiel für dieses Szenario ist ein Online-Shop von Adventure Works, der nur für den US-amerikanischen Markt eingerichtet ist.

Das folgende Beispiel zeigt eine Kanalkonfiguration in Commerce headquarters. In dieser Konfiguration unterstützt der Onlinekanal nur eine einzige Sprache (**en-us**), eine einheitliche Währung (**USD**) und eine einzelne Geschäftseinheit (**usrt**), die für die Steuererklärung verwendet wird.

![Juristische Person, Währung und Sprachwerte für den Adventure Works-Onlineshop, die in Commerce headquarters hervorgehoben sind.](media/channel-mapping-3.png)

Der einzelne Onlinekanal kann im Website-Generator einer einzelnen E-Commerce-Website zugeordnet werden. Informationen zum Erstellen einer neuen Website und zum Zuordnen zu einem Kanal finden Sie im Abschnitt [Einen Kanal einer Website im Website-Generator zuordnen](#map-a-channel-to-a-site-in-site-builder) dieses Artikels.

### <a name="multi-language-channel-that-has-a-single-localized-site-experience"></a>Ein mehrsprachiger Kanal, der eine einzige lokalisierte Website-Erfahrung bietet

In diesem Szenario unterstützt ein einzelner Kanal mehr als eine Sprache. Daher können Produktnamen, Beschreibungen und Attribute in Commerce headquarters lokalisiert werden. Um ein vollständig lokalisiertes Website-Erlebnis zu bieten, können Marketinginhalte auf der Website auch im Commerce-Website-Generator lokalisiert werden.

Die Einschränkung dieses Szenarios besteht darin, dass ein einzelner Kanal nur mit einer Währung, einer juristischen Person und einem Satz von Produkten und Preisen konfiguriert werden kann. Diese Konfiguration eignet sich am besten für Länder mit einer einzigen Währung und mehreren Sprachen (z. B. Kanada mit englischer und französischer Sprache), einer einzigen juristischen Person und einem einzigen Satz von Produkten und Preisen.

Jede Sprache in einem Kanal kann mit einem eigenen Domänennamen konfiguriert werden. Zum Beispiel kann die Domäne `www.adventure-works.ca` für die englische Version in Kanada konfiguriert werden, und die Domäne `www.adventure-works-fr.ca` kann für die französische Version in Kanada konfiguriert werden. Alternativ können verschiedene Sprachen in einem Kanal in einer einzigen Domäne konfiguriert werden, und dann kann für jede Sprache ein anderer Pfad verwendet werden. Zum Beispiel kann die Domäne `www.adventure-works.ca` für die englische Version in Kanada konfiguriert werden, und dann kann der Pfad `www.adventure-works.ca/fr` für die französische Version in Kanada konfiguriert werden. [Geo-Erkennung](geo-detection-redirection.md) kann auch aktiviert werden, um einen Benutzer basierend auf dem Standort des Benutzers automatisch auf die richtige Website umzuleiten.

Informationen dazu, wie Sie es Kunden ermöglichen, manuell zwischen Sprachen zu wechseln, finden Sie im Abschnitt [Websiteauswahlmodul hinzufügen und konfigurieren](#add-and-configure-the-site-picker-module) dieses Artikels. Informationen zum Anpassen lokalisierter Seiten und Fragmente finden Sie im Abschnitt [Website-Inhalte mit mehreren Kanälen und Sprachen verwalten](#manage-site-content-that-has-multiple-channels-and-languages).

### <a name="multi-language-channel-that-has-a-different-site-experience-per-language"></a>Ein mehrsprachiger Kanal, der eine andere Website-Erfahrung pro Sprache bietet

Möglicherweise bevorzugen Sie ein Szenario, in dem ein einzelner Kanal mehr als eine Sprache unterstützt, aber für jede Sprache eine völlig andere Website-Erfahrung gerendert wird. Die empfohlene Methode zum Implementieren dieses Szenarios ist die Verwendung von [Seitenvarianten](#implement-page-variants-for-each-language) auf einer einzigen Website.

Eine andere Methode besteht darin, im Website-Generator eine neue E-Commerce-Website für jede Sprache zu erstellen und dann jede Website einem einzelnen Onlinekanal und einer einzelnen Sprache zuzuordnen. Das Ergebnis wird ein einzelner Onlinekanal sein, der mehreren E-Commerce-Websites zugeordnet ist, einer für jede Sprache. Diese Methode mit mehreren Websites erfordert zusätzliche Verwaltungsressourcen, da mehr als eine Website im Website-Generator verwaltet werden muss.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-single-localized-site-experience"></a>Mehrere Kanäle (einsprachig und/oder mehrsprachig), die eine einzige lokalisierte Website-Erfahrung haben

Eine Marken-Website erfordert möglicherweise mehrere Online-Kanäle pro Region, um eine andere Währung, eine Reihe von Produkten und eine Reihe von Preisen für jeden Kanal auf einer einzigen Website zu unterstützen. Beispielsweise könnte die Adventure Works-Website einen Onlinekanal für den kanadischen Markt mit mehreren Sprachen, einen Kanal für den US-amerikanischen Markt mit einer Sprache und einen Kanal für den deutschen Markt mit einer Sprache haben. In diesem Szenario wird jeder Onlinekanal für eine regionsspezifische juristische Person konfiguriert und kann dieselben Produkte haben wie andere Kanäle, eine Teilmenge dieser Produkte oder eine andere Produktgruppe. Jeder Kanal hat auch seine eigenen Preise in der regionalen Währung, Steuern, Rabatte und Versandarten.

In diesem Szenario kann jeder Markt mit eigenen Domänennamen konfiguriert werden. Zum Beispiel kann die Domäne `www.adventure-works.com` für den US-amerikanischen Markt konfiguriert werden, und die Domäne `www.adventure-works.de` kann für den deutschen Markt konfiguriert werden. Alternativ kann jeder Markt so konfiguriert werden, dass er einen anderen Pfad verwendet. Zum Beispiel kann die Domäne `www.adventure-works.com` für den US-amerikanischen Markt konfiguriert werden, und dann kann der Pfad `www.adventure-works.com/de` für den deutschen Markt konfiguriert werden. [Geo-Erkennung](geo-detection-redirection.md) kann auch aktiviert werden, um Benutzer basierend auf ihrer Region automatisch auf die richtige Website umzuleiten.

Möglicherweise möchten Sie auch, dass Ihre Website eine Dropdown-Liste bereitstellt, mit der Benutzer manuell zu einem bestimmten Markt wechseln können. Weitere Informationen finden Sie im Abschnitt [Websiteauswahlmodul hinzufügen und konfigurieren](#add-and-configure-the-site-picker-module) dieses Artikels.

Informationen zum Konfigurieren mehrerer Kanäle auf einer einzelnen Website finden Sie im Abschnitt [Mehrere Kanäle auf einer E-Commerce-Website konfigurieren](#configure-multiple-channels-on-an-e-commerce-site).

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-different-site-experience-per-channel"></a>Mehrere Kanäle (einsprachig und/oder mehrsprachig), die eine einzige andere Website-Erfahrung pro Kanal haben

Möglicherweise möchten Sie mehrere Kanäle für eine einzelne Marke in verschiedenen Regionen haben, und Sie möchten möglicherweise, dass jede Region ein anderes Website-Erlebnis bietet. Es gibt zwei Methoden zur Implementierung dieses Szenarios:

- Sie können [Seitenvarianten](#implement-page-variants-for-each-language) verwenden.
- Konfigurieren Sie im Website-Generator für jeden Onlinekanal eine andere Website und ordnen Sie dann jede Website einem anderen Onlinekanal und einer anderen Sprache zu. Diese Methode erfordert zusätzliche Verwaltungsressourcen, da mehr als eine Website im Website-Generator verwaltet werden muss.

## <a name="cross-channel-sharing"></a>Kanalübergreifende Freigabe

Die kanalübergreifende Freigabe ist nützlich, wenn mehrere Kanäle auf einer Website Inhalte freigeben können. Beispielsweise kann ein Einzelhändler mit mehreren Marken und Ladenzeilen, die unter einer einzigen Website zusammengefasst sind, einige Inhalte für einige oder alle Ladenzeilen freigeben. Freigegebener Inhalt kann Seiten mit allgemeinen Geschäftsbedingungen, Zahlungsbedingungen, Versandmethoden und häufig gestellten Fragen (FAQ) enthalten. Weitere Informationen finden Sie unter [Kanalübergreifende Freigabe aktivieren und verwenden](cross-channel-sharing.md).

## <a name="map-a-channel-to-a-site-in-site-builder"></a>Einen Kanal einer Website im Website-Generator zuordnen

Es gibt mehrere Methoden zum Erstellen und Konfigurieren von Websites, um verschiedene Online-Kanäle zu verwenden.

### <a name="create-a-new-site"></a>Neue Website erstellen

Sie können eine brandneue Website im Website-Generator erstellen, indem Sie zur Seite mit der Liste **Websites** gehen und **Neue Website** auswählen. Dann können Sie im Dialogfeld **Neue Website** den Standard-Onlinekanal und die Standardsprache für die Website auswählen, wie in der folgenden Beispielabbildung gezeigt.

![Erstellen Sie einen neuen Kanal im Website-Generator.](media/channel-mapping-4.png)

Die Website, die Sie auf diese Weise erstellen, ist leer und enthält keine Website-Seiten (z. B. eine Startseite, Kategorieseiten und Produktseiten).

Weitere Informationen finden Sie unter [Eine E-Commerce-Website erstellen](create-ecommerce-site.md).

### <a name="create-a-new-site-by-using-the-site-copy-operation"></a>Neue Website durch Verwendung des Website-Kopiervorgangs erstellen

Anstatt eine brandneue, leere Website zu erstellen, wie im vorherigen Abschnitt beschrieben, ist es besser, mit einer Kopie einer der Starterwebsites zu beginnen, die in der Commerce-Modulbibliothek bereitgestellt werden, z. B. der Fabrikam- oder Adventure Works-Website.

Um eine vorhandene Website zu kopieren, gehen Sie zur Seite mit der Liste **Websites**, und wählen Sie **Website kopieren** aus. Dann können Sie im Dialogfeld **Website kopieren** die Quellwebsite auswählen und den Namen der Zielwebsite angeben.

Zu diesem Zeitpunkt können Sie den Standard-Onlinekanal und die Standardsprache für die Website noch nicht auswählen. Sie können diese Eigenschaften jedoch konfigurieren, nachdem der Website-Kopiervorgang abgeschlossen wurde. Wenn Sie die Website zum ersten Mal auf der Listenseite **Websites** im Website-Generator auswählen, wird das Dialogfeld **Website einrichten** angezeigt, auf dem Sie den Standardkanal und die Standardsprache auswählen können.

Weitere Informationen zum Website-Kopiervorgang finden Sie unter [E-Commerce-Website kopieren](copy-ecommerce-site.md).

### <a name="manage-an-existing-site-channel"></a>Vorhandenen Website-Kanal verwalten

Nachdem eine Website mit einem Kanal konfiguriert wurde, können Sie den Kanal innerhalb der ausgewählten Website im Website-Generator unter **Website-Einstellungen \> Kanäle** wie in der folgenden Beispielabbildung gezeigt verwalten und aktualisieren.

![Verwalten des Kanal-Mappings im Website-Generator.](media/channel-mapping-7.png)

## <a name="support-multiple-sites-in-a-single-tenant"></a>Mehrere Websites in einem einzigen Mandanten unterstützen

Viele Markenwebsites können in einem einzigen Mandanten koexistieren. Die folgende Beispielabbildung zeigt drei verschiedene Markenwebsites (Adventure Works, Adventure Works Business und Fabrikam), die jeweils einem anderen einzelnen Onlinekanal zugeordnet sind.

![Website-Liste im Website-Generator.](media/channel-mapping-8.png)

## <a name="configure-a-single-domain-name-with-paths-for-multiple-sites"></a>Einzelnen Domänennamen mit Pfaden für mehrere Websites konfigurieren

Ein einzelner Domänenname kann für mehrere Websites verwendet werden, und Pfade können dann verwendet werden, um Websites oder Sprachen zu trennen. Zum Beispiel ist die Domäne `www.mycompany.com` für zwei verschiedene E-Commerce-Websites konfiguriert: eine für Fabrikam und eine für Adventure Works. In diesem Fall ist der Standardpfad (`www.mycompany.com`), auch bekannt als leerer Pfad, kann für die Fabrikam-Website verwendet werden, und ein anderer Pfad (z. B. `www.mycompany.com/adventureworks`) kann für die Adventure Works-Website verwendet werden. Eine weitere Option ist die Verwendung eines benutzerdefinierten Pfads (z. B. `www.mycompany.com/fabrikam`) anstelle des Standardpfads auch für die Fabrikam-Website.

Alternativ kann für jede Website ein anderer Domänenname verwendet werden (z. B. `www.adventure-works.com` und `www.fabrikam.com`). Pfade können dann für verschiedene Sprachen oder Regionen verwendet werden (z. B. `www.adventure-works.com/fr-ca` für Kanada (Französisch)).

## <a name="configure-multiple-languages-on-a-site"></a>Mehrere Sprachen auf einer Website konfigurieren

Sprachen können für die E-Commerce-Website im Website-Generator unter **Website-Einstellungen \> Kanäle** konfiguriert werden. In der folgenden Beispielabbildung wurde jede Sprache mithilfe des Gebietsschemas für den Pfad konfiguriert, sodass jede Sprache über eine eindeutige URL verfügt.

![Mehrere Sprachen auf einer Website konfiguriert.](media/channel-mapping-10.png)

Um eine neue Kanalsprache hinzuzufügen, gehen Sie zu **Website-Einstellungen \> Kanäle**, und wählen Sie den Kanallink aus. Wählen Sie im rechts angezeigten Bereich **Gebietsschema hinzufügen** aus, um den Kanal und das Gebietsschema auszuwählen, den bzw. das Sie hinzufügen möchten. Geben Sie dann den Pfad an, der für den ausgewählten Kanal verwendet werden soll.

### <a name="add-and-configure-the-site-picker-module"></a>Websiteauswahlmodul hinzufügen und konfigurieren

Nachdem Sie eine Website mit mehreren Sprachen und/oder Kanälen konfiguriert haben, möchten Sie möglicherweise eine Sprachauswahl zur Seitenkopfzeile der Website hinzufügen, damit Benutzer ihre Sprache oder ihr Land manuell auswählen können. Die Modulbibliothek [Kopfzeilenmodul](author-header-module.md) verfügt über eine integrierte Unterstützung für Benutzer zur Auswahl einer Sprache mithilfe des [Websiteauswahlmoduls](site-selector.md). Das Websiteauswahlmodul kann dem Kopfzielenmodul des Kopfzeilenfragments hinzugefügt werden.

Weitere Informationen zum Hinzufügen und Konfigurieren des Websiteauswahlmoduls finden Sie unter [Websiteauswahlmodul](site-selector.md).

### <a name="implement-page-variants-for-each-language"></a>Seitenvarianten für jede Sprache implementieren

In diesem Szenario gibt es nur einen Kanal, aber mehrere Sprachen. Sie können das Erscheinungsbild einer Seite basierend auf der ausgewählten Sprache ändern, indem Sie eine Seitenvariante dafür erstellen. Anschließend können Sie der Variante lokalisierte Inhalte hinzufügen.

Wenn Sie eine Seite im Website-Generator geöffnet haben und den Link oben rechts auswählen, der den aktuellen Kanal und die aktuelle Sprache anzeigt, wird eine Kanal- und Sprachauswahl angezeigt, wie in der folgenden Beispielabbildung dargestellt. Wenn Sie die Seite für die aktuelle Sprache überschreiben möchten, wählen Sie ein anderes Gebietsschema und dann **Ändern** aus. Sie können auch den Kanal ändern, wenn Sie [eine Website mit mehreren Kanälen und Sprachen verwalten](#manage-site-content-that has-multiple-channels-and-languages).

![Ändern der Sprache für eine Seite im Website-Generator.](media/channel-mapping-14.png)

Wenn die Variante für die ausgewählte Seite oder das Fragment noch nicht erstellt wurde, erhalten Sie eine Warnmeldung, wie in der folgenden Beispielabbildung gezeigt. Wählen Sie in diesem Fall den Link **Seitenvariante erstellen** im Nachrichtentext aus. Das angezeigte Dialogfeld bietet Optionen, mit denen Sie entweder mit einer Kopie einer vorhandenen Variante beginnen oder eine brandneue Seite aus einer Vorlage erstellen können.

![Aufforderung zum Erstellen einer Seitenvariante im Website-Generator](media/channel-mapping-16.png)

Wenn Sie keine Variante erstellen, wird die Originalseite gerendert und zeigt die entsprechende Sprache für Modulzeichenfolgen und Produktinformationen aus Commerce headquarters an. Wenn jedoch Text wie ein Seitentitel oder andere Marketinginhalte direkt in Standardseitenmodulen angegeben wurden, bleiben die Zeichenfolgen für diesen Text in der Originalsprache.

Anstatt jede Seite und jedes Fragment manuell zu erstellen, können Sie jede Seite und jedes Fragment in eine XLIFF-Datei (XML Localization Interchange File Format) exportieren, die dann zur Lokalisierung gesendet werden kann. Nachdem jede XLIFF-Datei lokalisiert wurde, kann sie als lokalisierte Seitenvariante importiert werden. Um eine XLIFF-Datei von einer Seite oder einem Fragment im Website-Generator zu exportieren oder eine XLIFF-Datei in eine Seite oder ein Fragment zu importieren, wählen Sie **Lokalisierung** in der Befehlsleiste aus. Wählen Sie dann entweder **XLIFF exportieren** oder **XLIFF importieren** aus, wie in der folgenden Beispielabbildung gezeigt.

![Importieren oder Exportieren einer Seite oder eines Fragments im XLIFF-Format.](media/channel-mapping-18.png)

## <a name="manage-site-content-that-has-multiple-channels-and-languages"></a>Website-Inhalte mit mehreren Kanälen und Sprachen verwalten

Eine Website mit mehreren Kanälen und/oder Sprachen speichert eine eindeutige Variante jeder Seite und jedes Fragments für jede Kombination aus einem Kanal und einer Sprache. Dieses Verhalten ermöglicht es den Seitenvarianten, lokalisierte Daten zu enthalten, gibt Ihnen aber auch die Flexibilität, das Erscheinungsbild einer Seite für eine bestimmte Variante zu ändern.

Informationen zum Arbeiten mit Seitenvarianten finden Sie im Abschnitt [Seitenvarianten für jede Sprache implementieren](#implement-page-variants-for-each-language) dieses Artikels.

## <a name="configure-multiple-channels-on-an-e-commerce-site"></a>Mehrere Kanäle auf einer E-Commerce-Website konfigurieren

Sie können Kanäle zu einer E-Commerce-Website im Website-Generator hinzufügen, indem Sie zu **Website-Einstellungen \> Kanäle** gehen und **Kanal hinzufügen** auswählen. Anschließend können Sie im Dialogfeld **Kanal hinzufügen** den Onlinekanal und die Standardsprache auswählen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über Kanäle](channels-overview.md)

[Einen Onlinechannel einrichten](channel-setup-online.md)

[Organisationen und Organisationshierarchien – Übersicht](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md)

[Geo-Erkennung und -Umleitung einrichten](geo-detection-redirection.md)

[Aktivieren und verwenden Sie die kanalübergreifende Freigabe](cross-channel-sharing.md)

[E-Commerce-Site erstellen](create-ecommerce-site.md)

[Kopieren einer E-Commerce-Website](copy-ecommerce-site.md)

[Websiteauswahlmodul](site-selector.md)
