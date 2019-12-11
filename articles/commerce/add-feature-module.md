---
title: Funktionsmodul
description: Dieses Thema enthält Funktionsmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785283"
---
# <a name="feature-module"></a>Funktionsmodul 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema enthält Funktionsmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Ein Funktionsmodul wird verwendet, um Produkte oder verkaufsfördernden Maßnahmen über eine Kombination von Bildern und Text zu promoten. So kann beispielsweise ein Einzelhändler ein Funktionsmodul einer Produktdetailseite hinzufügen, um die Funktionen des Produkts hervorzuheben.

Ein Funktionsmodul wird durch Daten des Content Management-System (CMS) gesteuert. Es ist ein Stand-Alone-Module, das die nicht von Seiteninhalt oder anderen Modulen auf der Seite abhängt. Ein Funktionsmodul kann für jede beliebige Siteseite verwendet werden, in der ein Einzelhändler etwas promoten will (beispielsweise Produkte, Verkäufe oder Funktionen).

## <a name="examples-of-feature-modules-in-e-commerce"></a>Beispiele für Funktionsmodule in E-Commerce

Ein Funktionsmodul kann auf den folgenden Seiten verwendet werden:

- Eine Produktdetailseite, um Produktfunktionen zu zeigen
- Die Startseite, um Produkte zu promoten
- Eine Kategorieseite, um eine Produktgruppe zu markieren

## <a name="feature-module-properties"></a>Hinzufügen von Funktionseigenschaften

| Eigenschaftenname     | Werte | Beschreibung |
|-------------------|--------|-------------|
| Bild             | Bilddatei | Ein Bild kann verwendet werden, um ein Produkt oder eine verkaufsfördernde Aktion durchzuführen. Ein Bild kann zu der Bildergalerie hochgeladen werden, oder ein vorhandenes Bild kann verwendet werden. |
| Überschrift           | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Jedes Funktionsmodul kann eine Überschrift haben. Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet. Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen. |
| Absatz         | Absatztext | Funktionsmodule unterstützt Absatztext im Rich-Text-Format. Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung und Hyperlinks. Einige dieser Funktionen können vom Seitenthema überschrieben werden, das im Modul verwendet wird. |
| Verknüpfung              | Verknüpfen Sie Text, Link-URL, umfangreiche Internet-Anwendungs (ARIA)- Beschriftung und **Öffnen Sie die Verknüpfung in einer neuen Registerkarte** | Funktionsmomodul unterstützt mindestens einen oder mehrere Links „Aufruf zum Handeln“. Wenn ein Link hinzugefügt wird, sind der Linktext, eine URL und eine ARIA-Beschriftung erforderlich. ARIA-Beschriftungen sollen beschreibend sein, um Barrierefreiheitsbedingungen zu erfüllen. Links können konfiguriert werden, sodass sie auf einer neuen Registerkarte geöffnet werden. |
| Bildplatzierung   | **Rechts**, **Links**, **Oben** oder **Unten** | Diese Eigenschaft definiert die Bildlage relativ zum im Text. Wenn beispielsweise **Rechts** aktiviert ist, erscheint das Bild auf der rechten Seite des Texts. |
| Bild-Spaltengröße | Ein Wert von **1** bis **12** | Diese Eigenschaft definiert die Größe des Bildes relativ zum Text. Größe wird als Anzahl Spalten auf der Seite angegeben. Es gibt 12 Spalten auf einer Seite. Standardmäßig haben das Bild und der Text die gleiche Größe (je sechs Spalten). Allerdings kann die Größe nach Bedarf geändert werden. |

## <a name="add-a-feature-module-to-a-new-page"></a>Ein Funktionsmodul kann einer neuen Seite hinzugefügt werde 

Um ein Funktionsmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Vorlagen** und erstellen Sie eine Seitenvorlage mit der Bezeichnung **Funktionsvorlage**.
1. Im **Haupt-** Slot der Standardseite fügen Sie ein Funktionsmodul hinzu.
1. Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.
1. Verwenden Sie die Funktionsvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Funktionsseite** hat.
1. Auf dem Seitenüberblick wählen Sie den Slot (**Haupt**) und wählen die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Im Dialogfeld **Modul hinzufügen** unter **Modul wählen** wählen Sie das Funktionsmodul, und wählen Sie dann **OK**.
1. In der Gliederungsstruktur im Feld links wählen Sie das Funktionsmodul aus.
1. Wählen Sie im Eigenschaftenbereich rechts und wählen Sie **Eine Bild hinzufügen** aus. Wählen Sie dann ein vorhandenes Bild aus oder laden Sie ein neues Bild hoch.
1. Wählen Sie **Kopfzeile** aus.
1. Im Dialogfeld **Überschrift** fügen Sie den Überschriftentext hinzu, wählen Sie die Überschriftsebene, und wählen Sie dann **OK** aus.
1. Fügen Sie unter **Rich-Text** Text hinzufügen, wie Sie diesen benötigen.
1. Wählen Sie **Fügen Sie Aktivitäts-Link hinzu** aus.
1. Im Dialogfeld **Aktivitäts-Link** fügen Sie Text des Links, eine URL und eine ARIA-Beschriftung hinzu und wählen Sie dann **OK**.
1. Seite speichern und Ihre Änderungen in der Vorschau anzeigen.
1. Laden Sie die Seite hoch und veröffentlichen Sie sie.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Warnmmodul](add-alert.md)

[Karussellmodul](add-carousel.md)

[Umfangreiches Inhaltsblockmodul](add-content-rich-block.md)

[Inhaltsplatzierungsmodul](add-content-placement-modules.md)

[Hero-Modul](add-hero-module.md)

[Video-Player-Modul](add-video-player.md)
