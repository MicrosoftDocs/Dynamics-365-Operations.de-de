---
title: Voraussetzungen für die Standardkostenübersicht
description: In diesem Thema werden die grundlegenden Schritte zur Verwendung von Standardkosten beschrieben.
author: AndersGirke
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92f80ecc611e68210e24e59b696724e1bc9c3a06
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809661"
---
# <a name="prerequisites-for-standard-costs-overview"></a>Voraussetzungen für die Standardkostenübersicht

[!include [banner](../includes/banner.md)]

In diesem Thema werden die grundlegenden Schritte zur Verwendung von Standardkosten beschrieben. Die weiteren Schritte hängen von den Arbeitsgängen des Unternehmens ab. Diese Schritte unterscheiden sich beispielsweise bei einer Umgebung ohne Produktion, bei einer Produktionsumgebung, in der keine Routings verwendet werden, und bei einer Produktionsumgebung mit Routings. 

Gehen Sie zum Einrichten von Standardkosten folgendermaßen vor.

**1. Erstellen Sie eine Artikelmodellgruppe für Standardkosten.**

Erstellen Sie mithilfe der Seite **Artikelmodellgruppe** eine neue Gruppe für Standardkosten, und weisen Sie ein Lagermodell vom Typ **Standardkosten** zu. Geben Sie für die Artikelmodellgruppe einen aussagekräftigen Bezeichner, wie beispielsweise **Standardkosten** an. Legen Sie durch Aktivieren der Kontrollkästchen fest, dass für die Gruppe wertmäßig negativer Bestand, das Buchen physischen Bestands sowie das Buchen wertmäßigen Bestands zulässig sein soll. Diese Standardkostengruppe wird Artikeln zugewiesen.

**2. Definieren Sie Sachkonten, die sich auf Standardkostenabweichungen beziehen.** 

Definieren Sie mithilfe der Seite **Kontenplan** Sachkonten, die sich auf Standardkostenabweichungen beziehen. Diese Sachkonten müssen zunächst definiert werden, damit sie auf der Seite **Buchung** zugewiesen werden können. Sachkonten können sowohl für Artikelgruppen als auch für Kostengruppen stehen.

**3. Weisen Sie Artikelbuchungen, die sich auf Standardkostenabweichungen beziehen, Sachkonten zu.** 

Weisen Sie mithilfe der Seite **Buchung** die Sachkonten zu, die sich auf Standardkostenabweichungen beziehen. Sie können das Sachkonto einer Abweichung gemäß Artikel (oder Artikelgruppe) und Kostengruppe (oder Kostengruppentyp) angeben, oder Sie können angeben, dass das Sachkonto für alle Artikel und Kostengruppen gilt. Diese Optionen entsprechen den Kostenbeziehungen für „Tabellen”, „Gruppen” oder „Alle”. 

Bevor Sie die Artikelbuchungsregeln definieren, verwenden Sie die Seite **Buchungskombinationen**, um Kostenbeziehungen (für Tabellen, Gruppen und Alle) zu aktivieren.

**4. Definieren Sie Lagerparameter, die sich auf Standardkosten beziehen.** 

-  Definieren Sie mithilfe der Registerkarte **Bestandbuchhaltung** auf der Seite **Bestandbuchhaltungsrichtlinie einrichten > Parameter** zwei Kostensteuerungsparameter, die sich auf Standardkosten beziehen.

    -  Wählen Sie im Feld **Kostenaufschlüsselung** die Option **Keine** oder **Untergeordnetes Sachkonto** aus. Wenn Sie **Untergeordnetes Sachkonto** auswählen, ist die Kostenaufschlüsselung eine *aktive* Kostenaufschlüsselung. Eine aktive Kostenaufschlüsselung ist von entscheidender Bedeutung für die übergreifende Berechnung, Beibehaltung und Anzeige der Kostengruppensegmentierung in einer mehrstufigen Produktstruktur für Standardkostenartikel. Bei aktiver Kostenaufschlüsselung lassen sich Lagerbestand, Umlaufbestand (Ressourcen in Fertigung, RIF) sowie Wareneinsatz (Cost Of Goods Sold, COGS) pro Kostengruppe in einem einstufigen, mehrstufigen oder in einem Gesamtformat melden und analysieren. Sofern die Kostenaufschlüsselung aktiv ist, wenn Sie die Kosten eines produzierten Artikels aktivieren, wird die Kostengruppensegmentierung im Kostendatensatz des Artikels gespeichert. 

    -  Wenn Sie **Keine** auswählen, wird die Kostengruppensegmentierung für Standardkostenartikel nicht verwaltet. Das bedeutet, dass die Standardkosten eines produzierten Artikels als einzelner Betrag berechnet und verwaltet werden, ohne Kostengruppensegmentierung. Die Kostenbeiträge produzierter Komponenten werden in einem einzelnen Betrag zusammengeführt.

-  Wählen Sie im Feld **Abweichungen vom Standard** die Option **Zusammengefasst** oder **Pro Kostengruppe** aus. Wenn Sie die Option **Pro Kostengruppe** auswählen, können Sie Einkaufspreisabweichungen und Produktionsabweichungen nach Kostengruppe identifizieren. Sie können auch die vier Arten von Produktionsabweichungen identifizieren: die Losgröße, Menge, Preis und Ersatzabweichungen. Bei Auswahl von **Zusammengefasst** sind keine Abweichungen nach Kostengruppe ersichtlich, und auch die Erkennung der vier Typen von Produktionsabweichungen ist nicht möglich. Sie können lediglich eine zusammengefasste Produktionsabweichung anzeigen.

-  Die Richtlinie für Abweichungen vom Standard ist unabhängig von der Richtlinie für die Kostenaufschlüsselung. Anders ausgedrückt können Sie eine Kostenaufschlüsselungsrichtlinie von **Keine** auswählen und Abweichungen pro Kostengruppe auswählen, sodass die Produktionsabweichungen pro Kostengruppe immer noch erfasst werden.

**5. Erstellen Sie Nachkalkulationsversionen für Standardkosten.** 

Erstellen Sie mithilfe der Seite **Nachkalkulationsversionssetup** mindestens eine Nachkalkulationsversion für Standardkosten. Jede Nachkalkulationsversion muss mit dem Nachkalkulationstyp **Standardkosten** versehen werden. Darüber hinaus muss für den Inhalt die Berücksichtigung von Kostendaten ermöglicht werden.

**6. Bereiten Sie für einen vorhandenen Kunden die Verwendung von Standardkosten vor.** 

Kunden, die ihre vorhandenen Artikel auf ein Lagermodell vom Typ „Standardkosten” umstellen möchten, benötigen dafür die Seite **Standardkostenumrechnungen**.


<a name="related-topics"></a>Verwandte Themen
--------

[Standardkostenumrechnung – Überblick](standard-cost-conversion-overview.md)

### <a name="blogs"></a>Blogs

#### <a name="community-blogs"></a>Communityblogs

- [So richten SieStandardkosten für Direktmaterialien in Dynamics 365 for Finance and Operations ein](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [Standardmäßige direkte Lohnkosten in Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]