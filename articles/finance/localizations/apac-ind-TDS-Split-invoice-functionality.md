---
title: Funktionalität zum Teilen von Rechnungen
description: Dieses Thema beschreibt das Setup und die Funktionalität zum Teilen von Rechnungen nach Lieferadresse und Steuerkontonummer (TAN).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f9bb4db14cbb7c9abb33ccee532ed73b378317bb
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408354"
---
# <a name="split-invoice-functionality"></a>Funktionalität zum Teilen von Rechnungen

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt das Setup und die Funktionalität zum Teilen von Rechnungen nach Lieferadresse und Steuerkontonummer (TAN).

Wählen Sie auf der Seite **Kreditorenbuchhaltungsparameter** auf der Registerkarte **Allgemein** **Produktzugang** oder **Rechnung** aus, um einen Produktzugang oder eine Rechnung mit unterschiedlichen Lieferadressen und TAN auf der Seite **Bestellung** zu buchen und zu teilen. Die gebuchte Rechnung wird dann nach Lieferadresse und TAN aufgeteilt.

Legen Sie auf der Registerkarte **Sammelaktualisierung** unter dem Inforegister **Aufteilung basierend auf** in der Reihe **Lieferinformationen** die Option **Bestätigung**, **Kommissionierliste**, **Lieferschein** oder **Rechnung** auf **Ja**, um eine Bestätigung, Kommissionierliste, einen Lieferschein oder eine Rechnung zu buchen und aufzuteilen, in denen unterschiedliche Lieferadressen und TAN für unterschiedliche Rechnungspositionen auf der Seite **Auftrag** festgelegt sind. Die Rechnung wird dann zuerst nach Lieferadresse und dann nach TAN aufgeteilt.

> [!IMPORTANT]
> - Wenn keine Optionen für **Lieferinformationen** auf **Ja** festgelegt sind, wird die Rechnung als Einzelrechnung gebucht. Es erfolgt keine Rechnungsaufteilung.
> - Um einen Lieferschein zu teilen und zu buchen, bei dem die Rechnungspositionen unterschiedliche Lieferadressen und TAN haben, müssen Sie die Option **Lieferschein** für **Lieferinformationen** auf **Ja** setzen.
> - Um eine Rechnung zu teilen und zu buchen, bei der die Rechnungspositionen unterschiedliche Lieferadressen und TAN haben, müssen Sie die Option **Rechnung** für **Lieferinformationen** auf **Ja** setzen.
> - Um eine Rechnung zu teilen, bei der die Rechnungspositionen unterschiedliche Lieferadressen, aber die gleiche TAN haben, müssen Sie die Option **Rechnung** für **Lieferinformationen** auf **Nein** setzen. Die Rechnung wird dann nach Lieferadresse aufgeteilt.

## <a name="example"></a>Beispiel

In diesem Beispiel ist die Option **Rechnung** für **Lieferinformationen** auf der Registerkarte **Sammelaktualisierung** der Seite **Kreditorenkontenparameter** auf **Ja** gesetzt. Es wird eine Einkaufsrechnung mit dem folgenden Setup für Lieferadressen und TAN in den Positionen gebucht:

- **Artikelposition 1:** Lieferadresse 1, TAN ABCD12345A
- **Artikelposition 2:** Lieferadresse 1, TAN ABCD12345A
- **Artikelposition 3:** Lieferadresse 2, TAN ABCE12345B
- **Artikelposition 4:** Lieferadresse 3, TAN ABCD12345A

In diesem Fall wird die Originalrechnung in zwei Rechnungen aufgeteilt und folgendermaßen gebucht:

- Rechnung 1 wird für Artikelposition 1 und 2 gebucht, da beide Positionen dieselbe Lieferadresse und TAN haben.
- Rechnung 2 wird für Artikelposition 3 gebucht.
- Rechnung 3 wird für Artikelposition 4 gebucht.
