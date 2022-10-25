---
title: Proaktive Chat-Parameter des Commerce Chat-Moduls
description: Dieser Artikel beschreibt die proaktiven Chat-Parameter von Commerce Chat-Modulen in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: f3cff89a25ff84414e7fdd32cbb26404c2080187
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691071"
---
# <a name="commerce-chat-module-proactive-chat-parameters"></a>Proaktive Chat-Parameter des Commerce Chat-Moduls

[!include [banner](includes/banner.md)]

Dieser Artikel beschreibt die proaktiven Chat-Parameter des Commerce Chats mit Omnichannel for Customer Service und Commerce Chat mit Power Virtual Agents Chat-Module in Microsoft Dynamics 365 Commerce.

## <a name="proactive-chat-properties"></a>Proaktive Chat-Eigenschaften

Die proaktiven Chat-Eigenschaften befinden sich im Eigenschaftenbereich von Commerce Chat with Omnichannel for Customer Service und Commerce Chat mit Power Virtual Agents Module im Commerce-Website-Generator.

> [!NOTE]
> Standardmäßig sind alle hier aufgelisteten proaktiven Chat-Eigenschaften leer. Wir empfehlen Ihnen, mehr über diese Eigenschaften zu erfahren und sie nur bei Bedarf festzulegen. Dieser Ansatz trägt dazu bei, dass fehlerhafte proaktive Chats nicht ausgelöst werden.

### <a name="proactive-chat"></a>Proaktiver Chat

| Anzeigename | Description | Standardwert |
|---------------|-------------|---------------|
| Aktiviert | Binden Sie Kunden proaktiv ein, basierend auf verschiedenen Auslösern. | Deaktiviert |
| Chat-Begrüßung | Die Begrüßungsnachricht, die verwendet wird, wenn ein proaktiver Chat ausgelöst wurde. | Leer |

### <a name="wait-time-proactive-chat"></a>Wartezeit (proaktiver Chat)

| Anzeigename | Description |
|---------------|-------------|
| Wartezeit (sek) | Die Zeit (in Sekunden), die Site-Benutzer auf einer Site-Seite verbringen, bevor ein proaktiver Chat ausgelöst wird. |
| Chat-Begrüßung | Die Begrüßungsnachricht, die verwendet wird, wenn ein proaktiver Chat ausgelöst wurde. |

### <a name="number-of-page-visits-proactive-chat"></a>Anzahl der Seitenaufrufe (proaktiver Chat)

| Anzeigename | Description |
|---------------|-------------|
| Anzahl der Seitenaufrufe | Die Anzahl der Seitenbesuche, bevor ein proaktiver Chat ausgelöst wird. Site-Benutzer müssen zuerst die Aufforderung im Cookie-Zustimmungsbanner akzeptieren. |
| Chat-Begrüßung | Die Begrüßungsnachricht, die verwendet wird, wenn ein proaktiver Chat ausgelöst wurde. |

### <a name="specific-pages-proactive-chat"></a>Bestimmte Seiten (proaktiver Chat)

| Anzeigename | Description |
|---------------|-------------|
| Seite(n) | Eine Liste der Seiten, die einen proaktiven Chat auslösen, wenn sie besucht werden. |
| Chat-Begrüßung | Die Begrüßungsnachricht, die verwendet wird, wenn ein proaktiver Chat ausgelöst wurde. |

### <a name="from-specific-pages-proactive-chat"></a>Von bestimmten Seiten (proaktiver Chat)

| Anzeigename | Description |
|---------------|-------------|
| Seite(n) | Eine Liste der Seiten, die einen proaktiven Chat auslösen, wenn Benutzer von ihnen weg navigieren. |
| Chat-Begrüßung | Die Begrüßungsnachricht, die verwendet wird, wenn ein proaktiver Chat ausgelöst wurde. |

### <a name="specific-countryregion-proactive-chat"></a>Spezifisches Land/Region (proaktiver Chat)

| Anzeigename | Description |
|---------------|-------------|
| Ländercode | Benutzer, die aus bestimmten Ländern oder Regionen zu Besuch kommen, lösen einen proaktiven Chat aus. Land-/Regionscode sollten aus zwei Großbuchstaben bestehen (z. B.: **EU**). |
| Chat-Begrüßung | Die Begrüßungsnachricht, die verwendet wird, wenn ein proaktiver Chat ausgelöst wurde. |

### <a name="date-range-proactive-chat"></a>Datumsbereich (proaktiver Chat)

| Anzeigename | Description |
|---------------|-------------|
| Startdatum (TT/MM/JJJJ) | Das Datum, an oder nach dem ein proaktiver Chat ausgelöst wird. |
| Enddatum (TT/MM/JJJJ) | Das Datum, an oder vor dem ein proaktiver Chat ausgelöst wird. |
| Chat-Begrüßung | Die Begrüßungsnachricht, die verwendet wird, wenn ein proaktiver Chat ausgelöst wurde. |

### <a name="total-amount-in-cart-proactive-chat"></a>Gesamtbetrag im Warenkorb (proaktiver Chat)

| Anzeigename | Description |
|---------------|-------------|
| Minimum | Der minimale Geldbetrag (einschließlich) im Warenkorb, der einen proaktiven Chat auslöst, wenn Benutzer die Warenkorbseite besuchen. |
| Maximum | Der maximale Geldbetrag (einschließlich) im Warenkorb, der einen proaktiven Chat auslöst, wenn Benutzer die Warenkorbseite besuchen. |
|Chat-Begrüßung | Die Begrüßungsnachricht, die verwendet wird, wenn ein proaktiver Chat ausgelöst wurde. |

### <a name="total-number-of-items-in-cart-proactive-chat"></a>Gesamtzahl der Artikel im Warenkorb (proaktiver Chat)

| Anzeigename | Description |
|---------------|-------------|
| Minimum | Die minimale Anzahl an Artikeln (einschließlich) im Warenkorb, der einen proaktiven Chat auslöst, wenn Benutzer die Warenkorbseite besuchen. |
| Maximum | Die maximale Anzahl an Artikeln (einschließlich) im Warenkorb, der einen proaktiven Chat auslöst, wenn Benutzer die Warenkorbseite besuchen. |
| Chat-Begrüßung | Die Begrüßungsnachricht, die verwendet wird, wenn ein proaktiver Chat ausgelöst wurde. |

### <a name="specific-products-in-cart-proactive-chat"></a>Bestimmte Produkte im Warenkorb (proaktiver Chat)

| Anzeigename | Description |
|---------------|-------------|
| Produkt-ID/SKU | Eine Liste der Produkt-IDs/SKU-Nummern (Stock Keeping Unit), die einen proaktiven Chat auslösen, wenn Benutzer die Warenkorbseite besuchen. |
| Chat-Begrüßung | Die Begrüßungsnachricht, die verwendet wird, wenn ein proaktiver Chat ausgelöst wurde. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die E-Commerce-Chat-Funktionen](commerce-chat-overview.md)

[Modul „Commerce Chat mit Omnichannel for Customer Service“](commerce-chat-module.md)

[Commerce Chat mit Power Virtual Agents Modul](chat-module-pva.md)
