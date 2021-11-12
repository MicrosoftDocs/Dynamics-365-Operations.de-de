---
title: Modul zur Länder-/Regionsauswahl
description: Dieses Thema behandelt das Modul zur Länder-/Regionsauswahl und beschreibt, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 35d78cdcc356d35776940147e9b0afee0f0be2a2
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674722"
---
# <a name="countryregion-picker-module"></a>Modul zur Länder-/Regionsauswahl

[!include [banner](includes/banner.md)]

Dieses Thema behandelt das Modul zur Länder-/Regionsauswahl und beschreibt, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.

Das Modul zur Länder-/Regionsauswahl verwendet die Funktion [Geo-Erkennung und -Umleitung](geo-detection-redirection.md) in Dynamics 365 Commerce, um Debitoren URL-Empfehlungen anzuzeigen, die eine URL einer E-Commerce-Website anfordern, die nicht mit ihrem Land oder ihrer Region verknüpft ist.

Beispiel: Ein Debitor in Kanada fordert eine Website-URL an, die nicht mit Kanada verknüpft ist. In diesem Fall zeigt das Modul zur Länder-/Regionsauswahl ein Dialogfeld an, das Website-URLs empfiehlt, die mit Kanada verknüpft sind. In der folgenden Abbildung wird ein Beispiel des Dialogfelds „Länder-/Regionsauswahl“ angezeigt.

![Beispiel für ein Dialogfeld „Länder-/Regionsauswahl“ auf einer Homepage.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Eigenschaften des Moduls zur Länder-/Regionsauswahl

| Eigenschaftenname              | Wert       | Beschreibung |
| -------------------------- | ----------- | ----------- |
| Überschrift                    | Text        | Die Überschrift, die oben im Dialogfeld angezeigt wird. |
| Untertitel                 | Text        | Die Unterüberschrift, die unter der Überschrift angezeigt wird. |
| Land: Zeichenfolge der Anzeige    | Text        | Der Anzeigename für eine URL-Option (z. B. „Kanada“). |
| Land: Teilzeichenfolge der Anzeige | Text        | Eine optionale Teilzeichenfolge der Anzeige für eine URL-Option (z. B. „Englisch“ oder „Französisch“). |
| Land: Bild zum Land     | Medienobjekt | Ein optionales Bild, das einer URL-Option zugeordnet ist (z. B. ein Bild der kanadischen Flagge). |
| Land: Landes-URL       | Text        | Die URL, die dem Kanal und dem Gebietsschema entspricht, die für das Land oder die Region auf der Seite **Kanäle** im Commerce-Website-Generator konfiguriert sind (**Websiteeinstellungen \> Kanäle**). Diese URL muss genau mit der URL übereinstimmen, die auf der Seite **Kanäle** konfiguriert ist. |
| Aktivitätsverknüpfung                | Aktivitätsverknüpfung | Ein optionaler Link, der unten im Dialogfeld angezeigt wird. Dieser Link kann beispielsweise auf eine interne Seite verweisen, auf der alle Länder und Regionen angegeben sind, die von der Website unterstützt werden. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Hinzufügen eines Moduls zur Länder-/Regionsauswahl zu einer Seite

Das Modul zur Länder-/Regionsauswahl kann entweder direkt oder über ein freigegebenes Fragment zum Kopfzeilenmodul hinzugefügt werden. Weitere Informationen zu Kopfzeilenmodulen finden Sie unter [Kopfzeilenmodul](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Konfigurieren des Moduls zur Länder-/Regionsauswahl im Commerce-Website-Generator

> [!NOTE]
> Die URLs, die Sie Ihren Kunden empfehlen, müssen im Modul zur Länder-/Regionsauswahl als Länderobjekte konfiguriert sein.

Führen Sie für jede URL, die Sie Kunden anzeigen und empfehlen möchten, die folgenden Schritte im Commerce-Website-Generator aus.

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
