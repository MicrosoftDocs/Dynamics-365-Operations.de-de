---
title: Eine durch das Budget gesteuerte Bestellung erstellen
description: Erstellen Sie mit diesem Verfahren eine Bestellung, die auf einem verfügbaren Budget basiert.
author: JennySong-SH
ms.date: 06/15/2020
ms.topic: business-process
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa9777ad3aa487dfb558879335f93f347b8ac749
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016187"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Eine durch das Budget gesteuerte Bestellung erstellen

[!include [banner](../../includes/banner.md)]

Erstellen Sie mit diesem Verfahren eine Bestellung, die auf einem verfügbaren Budget basiert.

## <a name="review-the-budget-control-configuration"></a>Budgetsteuerungskonfiguration überprüfen.

1. Klicken auf **Budgetierung >Einrichtung > Budgetsteuerung > Budgetsteuerungskonfiguration**.
1. Wählen Sie die Registerkarte **Verfügbare Budgetmittel**.
1. Wählen Sie die **Dokument- und Erfassung**-Registerkarte.
1. Wählen Sie die Registerkarte **Budgetsteuerregel definieren**.
1. Wählen Sie die Registerkarte **Budgetgruppen definieren**.
1. Schließen Sie die Seite.

## <a name="create-a-purchase-order"></a>Eine Bestellung erstellen

1. Wechseln Sie zu **Beschaffung > Bestellung > Alle Bestellungen**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Kreditorenkonto** einen Wert ein, oder wählen Sie einen Wert aus.
1. Erweitern Sie das Inforegister **Allgemein**.
1. Legen Sie im Feld **Buchhaltungsdatum** das Datum fest.
1. Wählen Sie **OK** aus, um den Dialog zu schließen und Ihre neue Bestellung zu öffnen.
1. Wählen Sie auf dem **Bestellpositionen**-Inforegister in der Symbolleiste **Position hinzufügen** aus, um eine neue Zeile hinzuzufügen, und füllen Sie dann die Position nach Bedarf aus, um der Bestellung einen Artikel hinzuzufügen.
1. Wählen Sie in der Inforegister-Symbolleiste **Bestellpositionen** die Option **Finanzdaten \> Beträge verteilen** aus.
1. Geben Sie im Feld **Sachkonto** einen Betrag an.
1. Schließen Sie die Seite.

## <a name="perform-budget-checking"></a>Budgetprüfung ausführen

1. Fahren Sie mit der Bestellung fort, der Sie gerade eine Position hinzugefügt haben.
1. Wählen Sie in der Inforegister-Symbolleiste **Bestellpositionen** die Option **Finanzdaten \> Budgetprüfung ausführen** aus.
1. Wählen Sie in der Inforegister-Symbolleiste **Bestellpositionen** die Option **Finanzdaten \> Fehler oder Warnungen der Budgetprüfung** aus.
1. Das Dialogfeld **Formular für Fehler oder Warnungen der Budgetprüfung** wird geöffnet. Überprüfen Sie die Ergebnisse der Prüfung, und wählen Sie dann **Schließen** aus, um den Dialog zu schließen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]