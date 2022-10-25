---
title: Bestandspositionierung
description: Dieser Artikel enthält Informationen über die strategische Positionierung von Beständen, bei der es darum geht, Entkopplungspunkte in Ihrer Vorratskette zu identifizieren, an denen Sie Lagerbestände aufbauen können, um Vorlaufzeiten zu verkürzen und Schocks in Ihrer Vorratskette aufzufangen.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ReqGroup, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 847108575cbf7207282db00d731363c8cfad883a
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689537"
---
# <a name="inventory-positioning"></a>Bestandspositionierung

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Strategische Bestandspositionierung bedeutet, Entkopplungspunkte in Ihrer Vorratskette zu identifizieren, an denen Sie Lagerbestände aufbauen können. Dieser Ansatz wird hauptsächlich verwendet, um Vorlaufzeiten zu verkürzen und Schocks in Ihrer Vorratskette abzufedern. Es ermöglicht Ihnen die Behebung des „Bullwhip-Effekts“, da der schwankende Bedarf nicht über die gesamte Lieferkette weitergegeben wird. (Der *Bullwhip-Effekt* bezieht sich darauf, wie kleine Schwankungen des Bedarfs auf der Ebene des Einzelhandels zunehmend größere Schwankungen des Bedarfs auf der Ebene des Großhandels, der Distributoren, der Hersteller und der Rohstofflieferanten verursachen können.)

Die Bestandspositionierung ist der erste Schritt der bedarfsgesteuerten Ressourcenplanung (DDMRP).

## <a name="inventory-positioning-for-manufacturing"></a>Bestandspositionierung für die Fertigung

In diesem Abschnitt finden Sie ein Beispiel, das zeigt, wie Sie Entscheidungen zur Positionierung des Bestands treffen, wenn Sie ein typisches Kissenprodukt herstellen. Das Kissen verfügt über eine mehrstufige Stückliste (Stückliste), wie in der folgenden Abbildung dargestellt.

![Beispiel für eine mehrstufige Stückliste (Stückliste) für ein Kissenprodukt.](media/ddmrp-bom-example.png "Beispiel einer mehrstufigen Stückliste für ein Kopfkissenprodukt")

### <a name="choose-your-decoupling-points"></a>Wählen Sie Ihre Entkopplungspunkte

Wenn Sie auswählen, wo Sie Ihre Entkopplungspunkte platzieren möchten, berücksichtigen Sie alle folgenden Aspekte jedes Artikels in der Stückliste als Kriterien:

- Externe Variabilität
- Hebelwirkung und Flexibilität des Bestands
- Schutz kritischer Vorgänge
- Kunden-Toleranzzeit
- Sichtbarkeit von Verkaufsaufträgen
- Vorlaufzeit für Marktpotenzial

Im Kissen-Beispiel könnten Sie den ersten Entkopplungspunkt aus den folgenden Gründen beim *Schaumstoffknüppel* setzen:

- Es ist schwierig, die Materialien zu beschaffen, die zur Herstellung der Schaumstoffblöcke verwendet werden, und die Verfügbarkeit ist unbeständig. Daher ist das Kriterium *externe Variabilität* erfüllt.
- Die Schaumstoffknüppel können in viele verschiedene Formen und Größen geschnitten werden, um Schaumstoffeinlagen für andere Produkte zu erstellen, die Sie zusätzlich zum Kissen herstellen. Daher ist das Kriterium *Lagerhaltung und Flexibilität* erfüllt.

Sie könnten dann Ihren nächsten Entkopplungspunkt auf das *Stoffpaket* setzen, das aus vorgeschnittenem Kissenstoff besteht. Sie könnten diesen Punkt wählen, weil Sie nur eine Stoffschneidemaschine haben. Daher ist das Kriterium *Schutz kritischer Vorgänge* erfüllt.

Zum Schluss könnten Sie Ihren letzten Entkopplungspunkt bei dem Artikel fertige Ware Kissen setzen. Vielleicht wählen Sie diesen Punkt, weil Sie eine sehr geringe *Toleranzzeit* gegenüber dem Debitor haben und weil Ihr *Horizont für die Sichtbarkeit von Verkaufsaufträgen* recht kurz ist. Sie wollen also sicherstellen, dass Sie über den Lagerbestand verfügen, um die eingehenden Bestellungen zu erfüllen. Sie können auch einen höheren Preis festlegen, indem Sie die Vorlaufzeit so kurz halten, worauf sich das Kriterium *Marktpotenzial Vorlaufzeit* bezieht.

Auf der Grundlage dieser Analyse zeigt die folgende Abbildung, wie die Stückliste des Kissens aussehen wird. Gelbe Bestandssymbole markieren die Entkopplungspunkte.

![Beispiel Stückliste mit hervorgehobenen Entkopplungspunkten](media/ddmrp-bom-decoupling-example.png "Beispielstückliste mit hervorgehobenen Entkopplungspunkten")

### <a name="calculate-your-decoupled-lead-time"></a>Berechnen Sie Ihre entkoppelte Vorlaufzeit

Dieser Abschnitt zeigt, wie Sie Ihre neuen Vorlaufzeiten berechnen, nachdem Sie Entkopplungspunkte eingeführt haben.

In der folgenden Abbildung für das im vorigen Abschnitt begonnene Kissenbeispiel werden die Vorlaufzeiten in grauen Kästen oben links in jeder Stückliste angezeigt. Rot umrandete Kästchen kennzeichnen Artikel, die die kumulative Vorlaufzeit (die Summe der längsten Vorlaufzeiten auf jeder Ebene der Stückliste) bestimmen. Diese Vorlaufzeit beträgt 21 Tage, wenn Sie bei Null anfangen.

![Beispiel Stückliste mit Vorlaufzeiten.](media/ddmrp-bom-lead-times-example.png "Beispielstückliste mit Vorlaufzeiten")

Wenn Sie jedoch die Entkopplungspunkte anwenden, die Sie zuvor ausgewählt haben, werden die entkoppelten Artikel immer auf Lager sein. Sie werden daher eine Vorlaufzeit von 0 (Null) haben. Die neue Vorlaufzeit für das Kissen beträgt jetzt nur noch fünf Tage: zwei Tage für den Kauf des Garns und drei Tage für die Produktion des Kissens. Diese Vorlaufzeit wird als *entkoppelte Vorlaufzeit* bezeichnet.

![Beispiel für eine entkoppelte Vorlaufzeit.](media/ddmrp-bom-decoupled-lead-time-example.png "Beispiel für eine entkoppelte Vorlaufzeit")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>Strategische Bestandspositionierung in einem Einzelhandelsmodell

Da Einzelhändler nur fertige Produkte auf Lager haben, sind Stücklisten kein Thema. Einzelhändler können DDMRP jedoch weiterhin nutzen, indem sie die strategische Positionierung der Bestände und die Puffermengen auf der Grundlage der Lagerorte im Vertriebsnetz festlegen.

Die folgende Abbildung zeigt ein Beispiel für eine Firma, die ein Vertriebszentrum in Seattle und Stores in Boston, Atlanta und Portland hat.

![Entkopplungspunkte basierend auf der Lage in einem Einzelhandelsmodell.](media/ddmrp-retail-decoupl-points-example.png "Entkopplungspunkte basierend auf dem Standort in einem Einzelhandelsmodell")

Sie könnten zu dem Schluss kommen, dass die Transferzeit für den Transport eines Deckenprodukts zwischen dem Distributionszentrum und den Stores Ihre *Toleranzzeit für Kunden* verletzt, weil Ihre Debitor erwarten, dass die Decke auf Lager ist, wenn sie sie besuchen. In diesem Fall legen Sie in jedem der drei Stores einen Entkopplungspunkt für den Artikel Blanko fest. Jeder Store verfügt über unterschiedliche Puffer, je nach Vorlaufzeiten, Bedarf und so weiter.

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>Implementieren Sie die Bestandspositionierung in Dynamics 365 Supply Chain Management.

In diesem Abschnitt wird beschrieben, wie Sie Ihre Strategie zur Positionierung von Beständen in Microsoft Dynamics 365 Supply Chain Management implementieren.

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>Artikelabdeckungsgruppen festlegen, die Entkopplungspunkte erstellen

Artikel werden zu Entkopplungspunkten, wenn sie zu einer Abdeckungsgruppe gehören, die mit einem **Abdeckungscode**-Wert von *Entkopplungspunkt* konfiguriert ist. Der erste Schritt bei der Einrichtung von DDMRP besteht also darin, zu entscheiden, welche Abdeckungsgruppen Sie für Ihre DDMRP-Strategie implementieren müssen, und diese dann zu erstellen, indem Sie diese Schritte befolgen.

1. Gehen Sie zu **Produktprogrammplanung \> Einstellungen \> Planungshorizont \> Dispositionssteuerungsgruppen**
1. Wählen Sie im Aktionsbereich **Neu**, um eine Abdeckungsgruppe zu erstellen.
1. Geben Sie Informationen zur Identifizierung der Abdeckungsgruppe ein und wählen Sie dann den zu verwendenden Kalender.
1. Auf der Registerkarte **Allgemein** legen Sie im Feld **Abdeckungscode** den Wert *Entkopplungspunkt* fest. Diese Einstellung bewirkt, dass alle Artikel, die zu dieser Deckungsgruppe gehören, als Entkopplungspunkte für DDMRP behandelt werden. Außerdem werden alle DDMRP-Einstellungen für diese Gruppe aktiviert, wie später in diesem Verfahren beschrieben.
1. Auf der Registerkarte **Sonstiges**, im Abschnitt **DDMRP-Parameter**, legen Sie die folgenden Felder fest:

    - **Faktor für Vorlaufzeit** – Geben Sie einen Faktor (als Dezimalwert zwischen 0 und 1) an, um die Auswirkung zu steuern, die die Vorlaufzeit bei der Berechnung des Mindest- und Höchstbestands für Artikel in dieser Deckungsgruppe haben soll. Allgemein gilt: Je länger die Vorlaufzeit eines Artikels ist, desto niedriger sollte sein Vorlaufzeitfaktor sein. Ein niedriger Faktor für die Vorlaufzeit führt zu niedrigeren Mindest- und Höchstbeständen und damit zu kleineren und häufigeren Bestellungen. Die DDMRP-Methodik empfiehlt einen Wert zwischen 0,20 und 0,40 für Artikel mit langen Vorlaufzeiten, zwischen 0,41 und 0,60 für Artikel mit mittleren Vorlaufzeiten und zwischen 0,61 und 1,00 für Artikel mit kurzen Vorlaufzeiten. Weitere Informationen finden Sie unter [Pufferprofil und Ebenen](ddmrp-buffer-profile-and-levels.md).
    - **Variabilitätsfaktor** – Geben Sie einen Faktor an (als Dezimalwert zwischen 0 und 1), um die Auswirkung zu steuern, die ein schwankender Bedarf bei der Berechnung des Mindestbestands für Artikel in dieser Deckungsgruppe haben soll. Allgemein gilt: Je variabler der Bedarf eines Artikels ist, desto höher sollte sein Variabilitätsfaktor sein. Ein höherer Variabilitätsfaktor führt zu einem höheren Mindestbestand. Die DDMRP-Methodik empfiehlt einen Wert zwischen 0,00 und 0,40 für Artikel mit geringer Variabilität, zwischen 0,41 und 0,60 für Artikel mit mittlerer Variabilität und zwischen 0,61 und 1,00 für Artikel mit hoher Variabilität. Weitere Informationen finden Sie unter [Pufferprofil und Ebenen](ddmrp-buffer-profile-and-levels.md).
    - **Min., Max. und Wiederbestellpunktzeitraum** – Legen Sie fest, wie oft die Pufferwerte berechnet werden sollen (*Täglich* oder *Wöchentlich*).

1. Legen Sie auf der Registerkarte **Sonstiges** im Abschnitt **Durchschnittlicher täglicher Verbrauch** die folgenden Felder fest:

    - **Durchschnittlicher täglicher Verbrauch basierend auf** – Wählen Sie aus, auf welchen Zeiträumen die Berechnung des durchschnittlichen täglichen Verbrauchs (ADU) basieren soll. Wählen Sie einen der folgenden Werte aus:

        - *Vergangenheit* – Berücksichtigen Sie nur die vergangene Nutzung für die Anzahl der Tage, die im Feld **Vergangener Zeitraum (Tage)** angegeben sind. Die ADU wird berechnet als der Gesamtbedarf für einen Artikel während des Berechnungszeitraums (in Bestandseinheiten) geteilt durch die Anzahl der Tage im Berechnungszeitraum.
        - *Vorwärts* – Berücksichtigen Sie nur die prognostizierte zukünftige Nutzung (einschließlich Planungen) für die Anzahl der Tage, die im Feld **Vorwärtszeitraum (Tage)** angegeben sind. Die ADU wird berechnet als der Gesamtbedarf für einen Artikel während des Berechnungszeitraums (in Bestandseinheiten) geteilt durch die Anzahl der Tage im Berechnungszeitraum. 
        - *Gemischt* – Betrachten Sie sowohl die vergangene als auch die zukünftige Nutzung. Die Einstellungen für das Feld **Vergangener Zeitraum (Tage)**, das Feld **Weiterer Zeitraum (Tage)** und die Überblendungsoptionen sind alle festgelegt. 

            *Gemischte ADU* = (\[*Vergangenheitsgewichtung* × *Vergangenheits-ADU*\] + \[*Vorwärtsgewichtung* × *Vorwärts-ADU*\]) ÷ (*Vergangenheitsgewichtung* + *Vorwärtsgewichtung*)

    - **Vergangener Zeitraum (Tage)** – Geben Sie die Anzahl der vergangenen Tage (bis einschließlich heute) ein, die das System bei der Berechnung der ADU von Artikeln in dieser Erfassungsgruppe berücksichtigen soll. Diese Einstellung gilt nur, wenn das Feld **Durchschnittlicher täglicher Verbrauch basierend auf** auf *Vergangenheit* oder *Gemischt* festgelegt ist.
    - **Vorwärtsperiode (Tage)** – Geben Sie die Anzahl der zukünftigen Tage (ab heute und bis zum angegebenen Tag) ein, die das System bei der Berechnung der ADU von Artikeln in dieser Coverage Group berücksichtigen soll. Diese Einstellung gilt nur, wenn das Feld **Durchschnittlicher täglicher Verbrauch basierend auf** auf *Vorwärts* oder *Gemischt* festgelegt ist.
    - **Relative Gewichtung der vergangenen Periode für den durchschnittlichen täglichen Verbrauch (gemischt)** – Geben Sie die Gewichtung (in Prozent) ein, die für die vergangene Periode gelten soll, wenn der gemischte ADU berechnet wird. Diese Einstellung gilt nur, wenn das Feld **Durchschnittlicher täglicher Verbrauch basierend auf** auf *Gemischt* festgelegt ist.
    - **Relative Gewichtung der Vorwärtsperiode für den durchschnittlichen täglichen Verbrauch (gemischt)** – Geben Sie die Gewichtung (in Prozent) ein, die auf die Vorwärtsperiode angewendet werden soll, wenn der gemischte ADU berechnet wird. Diese Einstellung gilt nur, wenn das Feld **Durchschnittlicher täglicher Verbrauch basierend auf** auf *Gemischt* festgelegt ist.

1. Geben Sie für alle anderen Registerkarten und Felder die detaillierten Einstellungen ein, die für die Berechnung der Anforderungen für die Artikel verwendet werden, die mit dieser Deckungsgruppe verknüpft sind.

### <a name="set-an-item-as-a-decoupling-point"></a>Einen Artikel als Entkopplungspunkt festlegen

Um einen Artikel als Entkopplungspunkt festzulegen, gehen Sie folgendermaßen vor.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Suchen Sie einen zugelassenen Artikel, den Sie für DDMRP festlegen möchten, und wählen Sie ihn aus.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Plan** die Option **Artikelabdeckung**.
1. Auf der Seite **Artikelabdeckung** sind möglicherweise bereits mehrere Datensätze zur Artikelabdeckung aufgelistet, von denen jeder für eine andere Kombination von Lager- und Produktdimensionen gilt. Sie können einen bestehenden Datensatz zur Artikelabdeckung auswählen, der für die Dimensionen gilt, in denen Sie einen Entkopplungspunkt erstellen möchten. Alternativ können Sie **Neu** im Aktionsbereich wählen, um einen neuen Datensatz zur Artikelabdeckung zu erstellen.
1. Legen Sie den Datensatz für die Artikelabdeckung wie gewohnt fest. Sie müssen mindestens den Standort und das Lager angeben, für die der Entkopplungspunkt gelten soll.
1. Während der entsprechende Datensatz noch ausgewählt ist, wählen Sie die Registerkarte **Allgemein**.
1. Markieren Sie das Kontrollkästchen **Besondere Einstellungen verwenden**.
1. Setzen Sie das Feld **Deckungsgruppe** auf eine Deckungsgruppe, die für das Erstellen von Entkopplungspunkten festgelegt ist (wie im vorherigen Abschnitt beschrieben).
1. Der Artikel ist jetzt als Entkopplungspunkt konfiguriert. Wenn Sie DDMRP verwenden, werden Sie hier in der Regel auch Einstellungen festlegen, die sich auf die Puffergrößen und die Nachbestellmenge auswirken. Sie können diese Konfiguration jedoch auch später abschließen. Weitere Informationen zu den Einstellungen finden Sie unter [Puffer für einen Artikel der Entkopplungsstelle festlegen](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

> [!NOTE]
> Um Artikel zu planen, bei denen es sich nicht um Entkopplungspunkte handelt, befolgen Sie dieselben Schritte, die Sie bei der standardmäßigen Materialbedarfsplanung (MRP) durchführen.
