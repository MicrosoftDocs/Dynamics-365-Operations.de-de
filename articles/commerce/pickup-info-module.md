---
title: Abholinformationsmodul
description: Dieser Artikel behandelt das Abholinformationsmodul und beschreibt, wie es zu Auftragsabschlussseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 57633b7a23e581278ec0bc09ea146f5453570c4e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288405"
---
# <a name="pickup-information-module"></a>Abholinformationsmodul

[!include [banner](includes/banner.md)]

Dieser Artikel behandelt das Abholinformationsmodul und beschreibt, wie es zu Auftragsabschlussseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.

Das Abholinformationsmodul kann in einem Auftragsabschlussmodul verwendet werden, um Auftragsabholinformationen anzuzeigen. Kunden können verfügbare Abholtermine und Zeitfenster anzeigen und dann einen geeigneten Zeitpunkt für die Abholung ihres Auftrags auswählen. Beispielsweise kann ein Kunde auswählen, einen Auftrag um 15:00 Uhr am 21. März vom Geschäft in San Francisco abzuholen.

Die Abholzeitfenster für die entsprechenden Geschäfte müssen in der Commerce-Zentralverwaltung konfiguriert werden. Weitere Informationen finden Sie unter [Zeitfenster für die Kundenabholung erstellen und aktualisieren](dev-itpro/pickup-timeslots.md).

Wenn ein Abholinformationsmodul auf einer Auftragsabschlussseite erstellt wird, aber keine Zeitfenster für das Geschäft definiert sind, das für die Abholung ausgewählt wird, zeigt das Modul Informationen an, aber der Benutzer kann keine Zeitfenster auswählen. Zeitfenster sind optional und nicht erforderlich, um einen Auftrag zu erteilen.

Wenn mehrere Artikel für die Abholung in mehreren Filialen ausgewählt werden, ermöglicht das Abholinformationsmodul es dem Benutzer, ein Zeitfenster für jede Filiale auszuwählen, vorausgesetzt diese Zeitfenster sind für diese verfügbar.

> [!NOTE]
> Unterstützung für Zeitfenster und das Auftragsabschluss-Abholinformationsmodul ist in Dynamics 365 Commerce Version 10.0.15 und höher verfügbar.

Die folgende Abbildung zeigt ein Beispiel für die Auswahl eines Zeitfensters über das Abholinformationsmodul auf einer Auftragsabschlussseite.

![Beispiel eines Abholinformationsmoduls auf einer Auftragsabschlussseite.](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>Moduleigenschaften

- **Überschrift** – Geben Sie eine Überschrift für das Modul ein.

## <a name="show-time-slot-information-after-an-order-is-placed"></a>Zeigen Sie Zeitfensterinformationen an, nachdem ein Auftrag erteilt wurde

Nachdem ein Auftrag erstellt wurde, können Informationen zum ausgewählten Zeitfenster im [Auftragsbestätigungsmodul](order-confirmation-module.md) und im [Auftragsdetailmodul](account-management.md#order-details-page) angezeigt werden. Diese beiden Module haben die Eigenschaft **Zeitfensterinformationen anzeigen**. Bevor sie das ausgewählte Zeitfenster während des Auftragsprozesses anzeigen können, muss diese Eigenschaft auf **True** festgelegt sein.

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>Ein Auftragsabholinformationsmodul zu einer Seite hinzufügen

Anweisungen zum Hinzufügen eines Abholinformationsmoduls zu einer Auftragsabschlussseite und zum Festlegen der erforderlichen Eigenschaften finden Sie unter [Auftragsabschlussmodul](add-checkout-module.md).

Die folgende Abbildung zeigt ein Beispiel für eine E-Commerce-Auftragsabschlussseite, die Zeitfenster für Abholpositionsartikel enthält.

![Beispiel für eine E-Commerce-Auftragsabschlussseite, die Zeitfenster für Abholpositionen enthält.](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Zeitfenster für die Kundenabholung erstellen und aktualisieren](dev-itpro/pickup-timeslots.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Auftragsdetailmodul](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
