---
title: Nummern von TDS-Konzessionszertifikaten erfassen
description: In diesem Artikel wird erklärt, wie die für Kreditoren ausgestellten Nummern von Konzessionszertifikaten für die Quellenbesteuerung (TDS) erfasst werden.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 116bc5c4b4f5f0b95d05dc73f2a012fbbc065bf2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846612"
---
# <a name="record-tds-concession-certificate-numbers"></a>Nummern von TDS-Konzessionszertifikaten erfassen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erklärt, wie die für Kreditoren ausgestellten Nummern von Konzessionszertifikaten für die Quellenbesteuerung (TDS) erfasst werden.

1. Gehen Sie zu **Steuer \> Indirekte Steuern \> Quellensteuer \> Quellensteuerkonzessionen**.
2. Wählen Sie im Feld **Steuertyp** **TDS** aus, um Konzessionszertifikate für den Steuertyp „TDS“ zu erfassen.
3. Wählen Sie auf der Registerkarte **Übersicht** **ALT + N** aus, um eine Position zu erstellen.

    [![Kopfzeile der neuen Position.](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)

4. Wählen Sie im Feld **Quellensteuercode** den TDS-Steuercode aus, für den die Kreditorenkonzessionszertifikate ausgestellt werden. Im Feld **Quellensteuercodename** wird der Name des TDS-Steuercodes angezeigt.
5. Legen Sie in den Feldern **Startdatum** und **Enddatum** den Gültigkeitszeitraum für das Konzessionszertifikat fest, das der TDS-Steuercode verwendet, um die TDS für den Kreditor auf Konzessionsbasis zu berechnen.
6. Geben Sie im Feld **Hinweis** etwaige Hinweise ein.
7. Geben Sie im Feld **Abschnitt** den rechtlichen Abschnittscode ein, unter dem das TDS-Konzessionszertifikat verwendet wird.

    Wenn der Abschnittscode 197 lautet, wird der Wert „A“ sowohl in der Spalte „Grund für Nichtabzug/niedrigeren Abzug“ im Formular 26Q als auch in der Spalte „Grund für (gegebenenfalls) Nichtabzug/niedrigeren Abzug/Hochrechnung“ im Formular 27Q angezeigt. Wenn der Abschnittscode 197A lautet, wird an beiden Stellen der Wert „B“ angezeigt.

8. Wählen Sie das Inforegister **Zertifikat** aus, um TDS-Konzessionszertifikatnummern für Kreditoren zu erfassen.
9. Wählen Sie im Feld **Kreditorenkonto** das Kreditorenkonto aus, für das das TDS-Konzessionszertifikat ausgestellt wurde.
10. Legen Sie in den Feldern **Startdatum** und **Enddatum** die Gültigkeitsdauer des TDS-Konzessionszertifikats fest.

    Die Berechnung der TDS auf Konzessionsbasis basiert auf dem Zeitraum, in dem das Zertifikat für den Kreditoren erstellt wird.

11. Geben Sie im Feld **Zertifikatnummer** die TDS-Konzessionszertifikatsnummer ein.

    [![Inforegister „Zertifikat“.](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)

12. Schließen Sie die Seite.
