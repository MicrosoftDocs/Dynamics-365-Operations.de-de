---
title: Modul zur Länder-/Regionsauswahl
description: Dieses Thema behandelt das Modul zur Länder-/Regionsauswahl und beschreibt, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.
author: stuharg
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 9c20e614053b7a79cf962990dbd13ca0f45d5a00
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551669"
---
# <a name="countryregion-picker-module"></a>Modul zur Länder-/Regionsauswahl

[!include [banner](includes/banner.md)]

Dieses Thema behandelt das Modul zur Länder-/Regionsauswahl und beschreibt, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.

Das Modul zur Länder-/Regionsauswahl verwendet die Funktion [Geo-Erkennung und -Umleitung](geo-detection-redirection.md) in Dynamics 365 Commerce, um Kund\*innen Website-Empfehlungen anzuzeigen, die eine URL einer E-Commerce-Website anfordern, die nicht mit ihrem Land oder ihrer Region verknüpft ist.

Beispiel: Kund\*innen in Kanada fordern eine Website-URL an, die mit einem anderen Land als Kanada verknüpft ist. In diesem Fall zeigt das Modul zur Länder-/Regionsauswahl ein Dialogfeld an, das Website-URLs empfiehlt, die mit Kanada verknüpft sind. 

## <a name="how-it-works"></a>Funktionsweise

Wenn die geografische Erkennung und Weiterleitung für eine Website aktiviert sind und Kund\*innen eine Website-URL anfordern, wird anhand des für die Kund\*innen erkannten Landes und der angeforderten URL ermittelt, ob diese URL dem Land zugeordnet ist, in dem sich die Kund\*innen befinden. Die Zuordnung zwischen URLs und Ländern wird auf der Seite **Kanäle** unter **Websiteeinstellungen** im Commerce-Website-Generator definiert. 

Wenn die Anforderungs-URL mit keiner URL übereinstimmt, die dem Land der Kund\*innen zugeordnet ist, wird die Liste mit einer oder mehreren URLs, die diesem Land zugeordnet sind, in der Antwort zurückgegeben. Die Länder-/Regionsauswahl vergleicht jede URL in dieser Liste mit den URLs, die im Länder-/Regionsmodul konfiguriert wurden. Für jede exakte Übereinstimmung, die gefunden wird, rendert die Länder-/Regionsauswahl die angezeigte Überschrift, Unterüberschrift sowie das Bild für diese URL und verlinkt diese Elemente mithilfe der URL.

Wenn Kund\*innen eine Option in der Länder-/Regionsauswahl auswählen, werden sie zur verlinkten URL weitergeleitet. Diese URL wird in den Cookie **\_msdyn365\_\_\_site\_** geschrieben, damit es als Websitepräferenz der betreffenden Kund\*innen verwendet werden kann. Wenn Kund\*innen dann das nächste Mal die URL anfordern, die nicht mit ihrem Land oder ihrer Region verknüpft ist, werden sie automatisch zu ihrem bevorzugten Land umgeleitet. Daher empfehlen wir Ihnen, auch das [Websiteauswahlmodul](site-selector.md) auf Ihrer E-Commerce-Website zu verwenden, damit Kund\*innen ihre Website-Präferenz überschreiben oder aktualisieren können. 

Wenn Kund\*innen das Dialogfeld zur Länder-/Regionsauswahl schließen, wird kein Cookie geschrieben, und die Kund\*innen verbleiben auf der aktuellen Website. 

In der folgenden Abbildung wird ein Beispiel des Dialogfelds „Länder-/Regionsauswahl“ angezeigt.

![Beispiel für ein Dialogfeld „Länder-/Regionsauswahl“ auf einer Homepage.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Eigenschaften des Moduls zur Länder-/Regionsauswahl

| Eigenschaftenname              | Wert       | Beschreibung                                                  |
| -------------------------- | ----------- | ------------------------------------------------------------ |
| Überschrift                    | Text        | Die Überschrift, die oben im Dialogfeld angezeigt wird.       |
| Untertitel                 | Text        | Die Unterüberschrift, die unter der Überschrift angezeigt wird.               |
| Land: Zeichenfolge der Anzeige    | Text        | Der Anzeigename für eine URL-Option (z. B. „Kanada“).   |
| Land: Teilzeichenfolge der Anzeige | Text        | Eine optionale Teilzeichenfolge der Anzeige für eine URL-Option (z. B. „Englisch“ oder „Französisch“). |
| Land: Bild zum Land     | Medienobjekt | Ein optionales Bild, das einer URL-Option zugeordnet ist (z. B. ein Bild der kanadischen Flagge). |
| Land: Landes-URL       | Text        | Die Website-URL für das Land/die Region, die konfiguriert wird. Diese URL muss genau mit der URL übereinstimmen, die Sie für dieses Land/diese Region auf der Seite **Kanäle** unter **Websiteeinstellungen** im Commerce-Website-Generator angegeben haben. Außerdem muss die Domäne der URL die angepasste Domäne sein, die im Feld **Domain abgleichen** auf der Seite **Kanäle** angegeben ist, nicht die Arbeitsadresse der Website, die Commerce bereitstellt, wenn Sie Ihre E-Commerce-Umgebung erstellen (z. B. die URL `https://<yourcompany>.commerce.dynamics.com/`). |
| Aktivitätsverknüpfung                | Aktivitätsverknüpfung | Ein optionaler Link, der unten im Dialogfeld angezeigt wird. Dieser Link kann beispielsweise auf eine interne Seite verweisen, auf der alle Länder und Regionen angegeben sind, die von der Website unterstützt werden. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Hinzufügen eines Moduls zur Länder-/Regionsauswahl zu einer Seite

Das Modul zur Länder-/Regionsauswahl kann entweder direkt oder über ein freigegebenes Fragment zum Kopfzeilenmodul hinzugefügt werden. Weitere Informationen zu Kopfzeilenmodulen finden Sie unter [Kopfzeilenmodul](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Konfigurieren des Moduls zur Länder-/Regionsauswahl im Commerce-Website-Generator

> [!NOTE]
> Die URLs, die Sie Ihren Kunden empfehlen, müssen im Modul zur Länder-/Regionsauswahl als Länderobjekte konfiguriert sein.

Führen Sie für jede Website-URL, die Sie Kund\*innen anzeigen und empfehlen möchten, die folgenden Schritte im Commerce-Website-Generator aus.

1. Wählen Sie den Slot des Moduls zur Länder-/Regionsauswahl aus.
1. Wählen Sie im Eigenschaftenbereich unter **Länderliste** die Option **Land hinzufügen** aus.
1. Wählen Sie das Feld **Neues Land** aus.
1. Geben Sie in das Feld **Zeichenfolge der Anzeige** einen Anzeigenamen ein (z. B. **Kanada**).
1. Optional: Geben Sie in das Feld **Teilzeichenfolge der Anzeige** eine Teilzeichenfolge der Anzeige ein (z. B. **Französisch** oder **fr-ca**).
1. Optional: Wählen Sie ein Bild aus der Medienbibliothek aus.
1. Geben Sie in das Feld **Landes-URL** die URL ein. Diese URL muss genau mit der URL übereinstimmen, die auf der Seite **Kanäle** angezeigt wird und dem Kanal zugeordnet ist, einschließlich des Gebietsschemas, das mit dem Land oder der Region verknüpft ist. 
1. Wählen Sie **OK** aus.
1. Wiederholen Sie diese Schritte für alle anderen Länder-URLs, die das Modul zur Länder-/Regionsauswahl anzeigen soll.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Geo-Erkennung und -Umleitung einrichten](geo-detection-redirection.md)

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Kopfzeilenmodul](author-header-module.md)

[Websiteauswahlmodul](site-selector.md)

[Breadcrumb-Modul](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
