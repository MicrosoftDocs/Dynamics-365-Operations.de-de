---
title: Client wurde getrennt
description: In diesem Artikel wird erläutert, was zu tun ist, wenn der Kunde/die Kundin von seiner/ihrer Umgebung getrennt ist und den Grund nicht kennt.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d02916283bbd4cee6502942020df1b275a0242b3
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112699"
---
# <a name="client-disconnects"></a>Client wurde getrennt

**Umgebungsdetails** 

Dieses Problem kann in allen Umgebungen auftreten.
 
**Symptom** 

Der Kunde/die Kundin ist von seiner/ihrer Umgebung getrennt und kennt den Grund nicht. Der Kunde erhält eine der folgenden Fehlermeldungen:

- Die Verbindung wurde getrennt Klicken Sie auf „Schließen”, um die Arbeit fortzusetzen.
- Die Netzwerkverbindung wurde anscheinend unterbrochen. Klicken Sie auf 'Wiederholen', um es erneut zu versuchen.

**Rote Markierung**

Dieses Problem tritt häufig auf, wenn Benutzer sich in der Implementierungsphase befinden, nachdem sie Informationen über Produktions- und Testumgebungen hinweg verglichen haben und dabei vergessen, dass sie sich zwischen Sitzungen hin- und herbewegen. Wenn Benutzer in dieser Phase sind, erfahren sie höchstwahrscheinlich dieses Problem.

**Abgang** 

**Browsertypen:** Google Chrome, Internet Explorer und Microsoft Edge

Microsoft Dynamics 365 Human Resources trennt die Verbindung von Benutzern, wenn verschiedene Sitzungen gleichzeitig für denselben Benutzer und denselben Browsertyp geöffnet sind. (Benutzer A zeigt beispielsweise sowohl Umgebung 1 als auch Umgebung 2 in Chrome an.) Es spielt keine Rolle, ob die Benutzer verschiedene Browserfenster oder Registerkarten öffnen. Wenn dieselben Benutzeranmeldeinformationen verwendet werden, um sich sowohl in Umgebung 1 als auch in Umgebung 2 gleichzeitig und im selben Browsertyp anzumelden, trennt Human Resources die Verbindung für eine der Sitzungen.

**Lösung**

Stellen Sie sicher, dass nur eine Umgebung gleichzeitig für einen bestimmten Browsertyp geöffnet ist. Benutzer können mehrere Sitzungen für die gleiche Umgebung öffnen (das heißt, mehrere Registerkarten im selben Browser).

Benutzer, die zwischen zwei Umgebung gleichzeitig hin- und herwechseln möchten, sollten jede Umgebung in einem anderen Browsertyp öffnen. (Beispielsweise kann Benutzer A Umgebung 1 in Chrome und Umgebung 2 in Microsoft Edge anzeigen.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]