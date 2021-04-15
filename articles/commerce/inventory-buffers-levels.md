---
title: Konfigurieren Sie Inventarpuffer und Inventarebenen
description: In diesem Thema wird erläutert, wie Sie Inventarpuffer und Inventarebenen konfigurieren, die die Nachrichten zur Inventarverfügbarkeit auf Microsoft Dynamics 365 Commerce Websites bestimmen.
author: boycezhu
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: ca6cea9e0e7f1fd3eba3082c5a33e8b2d6dec878
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798912"
---
# <a name="configure-inventory-buffers-and-inventory-levels"></a>Bestandpuffer und Bestandsebenen konfigurieren

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Inventarpuffer und Inventarebenen konfigurieren, die die Nachrichten zur Inventarverfügbarkeit auf Microsoft Dynamics 365 Commerce-Websites bestimmen.

Dynamics 365 Commerce Zentralen befinden sich Inventardaten und verschiedene Kanäle wie POS-Anwendungen (Point of Sale), E-Commerce-Storefronts und andere benutzerdefinierte integrierte Anwendungen, mit denen Inventar asynchron abgerufen und verschoben werden kann. Daher sind die verfügbaren Inventarwerte, die über die vorhandene Inventarseite in der Commerce-Zentrale, über die POS-Benutzeroberfläche (UI) und über E-Commerce-APIs für die Verfügbarkeit von Inventar abgerufen werden, in Echtzeit nicht immer zu 100 Prozent genau.

Anstatt die tatsächlichen Inventarwerte in E-Commerce-Geschäften anzuzeigen, ziehen es viele Einzelhändler vor, nur Nachrichten über den Status der Inventarverfügbarkeit anzuzeigen (z. B. Verfügbar oder Nicht verfügbar), um Kunden darüber zu informieren, ob ein Artikel zum Kauf verfügbar oder möglicherweise nicht verfügbar ist auf Lager. Für diesen Ansatz müssen Inventarpuffer und Inventarebenen, die das Inventarverfügbarkeits-Messaging bestimmen, verfügbar gemacht und konfiguriert werden.

## <a name="prerequisite-turn-on-the-inventory-buffers-and-inventory-levels-feature"></a>Voraussetzung: Aktivieren Sie die Funktion Inventarpuffer und Inventarebenen

Die Funktion für Inventarpuffer und Inventarebenen wird über die Funktionsverwaltung in der Commerce-Zentrale gesteuert. Um die Funktion zu aktivieren, führen Sie diese Schritte aus.

1. Wechseln Sie zu **Systemverwaltung** \> **Arbeitsbereiche** \> **Datenverwaltung**.
1. Suche nach der Funktion **Aktivieren Sie Inventarpuffer und Inventarebenen**, wählen Sie die Zeile aus und wählen Sie dann **Jetzt aktivieren**.

Nachdem die Funktion aktiviert wurde, finden Sie die Lagerbestände unter **Einzelhandel und Handel \> Bestandsverwaltung**.

## <a name="create-and-configure-an-inventory-level-profile"></a>Erstellen und konfigurieren Sie ein Profil auf Inventarebene

Ein *Profil auf Inventarebene* legt fest, ob ein bestimmter Produktmengenstatus als auf Lager, nicht auf Lager oder in einem anderen benutzerdefinierten Status betrachtet wird. Sie können mehrere Profile auf Inventarebene pro juristischer Person erstellen und konfigurieren. Jedes Profil besteht aus einer Reihe von Inventarebenen, und jede Ebene wird durch ein *Angebot*, einen *Code*, und einer *Beschriftung* definiert.

- **Bereich** – Jeder Bereich wird durch eine *Startmenge* und ein *Endmenge* definiert Ein Mengenwert fällt in einen Bereich, wenn er größer als die Startmenge dieses Bereichs und nicht größer als die Endmenge ist.
- **Code** – Ein Code ist eine interne Abkürzung, die die Ebene darstellt. Kunden, die direkt in die Inventar-APIs integriert sind, können mithilfe von Codes zusätzliche Logik für eine bestimmte Inventarebene erstellen. Beispielsweise können sie die Kauffunktion für ein Produkt deaktivieren, wenn der Bestandscode **OOS** (nicht vorrätig) lautet.
- **Etikett** – Ein Etikett ist eine aussagekräftige kundenorientierte Nachricht, die Kunden auf einer E-Commerce-Website einen Lagerbestand vermittelt.

### <a name="create-an-inventory-level-profile"></a>Erstellen Sie ein Profil auf Inventarebene

Um ein Lagerbestandsprofil zu erstellen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Einzelhandel und Handel** \> **Bestandsverwaltung** \> **Lagerbestände**.
1. Wählen Sie im Aktionsbereich **Neu** und geben Sie dann Werte in das Feld **Profil ID** und **Beschreibung** ein.
1. Auf der Infoseite **Bereiche** wählen Sie **Hinzufügen**, um eine neue Ebene hinzuzufügen, und geben Sie dann Werte in die Spalten **Startmenge**, **Endmenge**, **Code**, und **Etikette** für diese Ebene ein. Wiederholen Sie diesen Schritt, um weitere Ebenen hinzuzufügen. Bei Bedarf können Sie die Werte im Datenraster bearbeiten oder **Löschen** auswählen, um eine Ebene zu entfernen.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Wenn ein neues Profil erstellt wird, werden automatisch zwei Inventarebenen initialisiert:

- **OOS** – Die Stufe Nicht vorrätig, bei der die Untergrenze des Bereichs negativ unendlich ist. Die Startmenge und der Code können für diese Ebene nicht bearbeitet werden.
- **VERFÜGBAR** – Die verfügbare Ebene, bei der die Obergrenze des Bereichs unendlich ist. Die Endmenge und der Code können für diese Ebene nicht bearbeitet werden.

> [!NOTE]
> Es darf keine Lücken oder Überlappungen zwischen Bereichen in der Profildefinition geben.

Sie können die Schaltfläche **Übersetzungen** im Aktionsbereich verwenden, um lokalisierte Zeichenfolgen für die Beschriftungsnachricht zu konfigurieren. Sie müssen dann den Verteilungszeitplan-Einzelvorgang **1110** (**Globale Konfiguration**) ausführen, um die lokalisierten Zeichenfolgen für Kanäle zu synchronisieren.

### <a name="configure-an-inventory-level-profile"></a>Konfigurieren Sie ein Profil auf Inventarebene

Sie können ein Inventarebenenprofil entweder auf Produktkategorieebene oder auf der Ebene der einzelnen Produkte konfigurieren. Wenn ein Inventarebenenprofil für ein Produkt konfiguriert ist, wird die Inventarebene basierend auf den Bereichen bestimmt, die im verknüpften Profil definiert sind. Andernfalls wird der Lagerbestand verfügbar oder nicht verfügbar basierend darauf bestimmt, ob das Produkt eine positive Lagerbestandsmenge aufweist.

Um ein Lagerbestandsprofil für eine Kategorie zu konfigurierenellen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Retail and Commerce** \> **Produkte und Kategorien** \> **Commerce-Produkthierarchie**.
1. Wählen Sie die Kategorie, um ein Lagerbestandsprofil zu konfigurieren.
1. Auf dem Inforegister **Verkaufen Sie Produkteigenschaften** wählen Sie eine juristische Person aus.
1. In dem Abschnitt **Commerce Bestand** im Feld **Profil auf Bestandebene** wählen Sie im Feld eines der vordefinierten Profile auf der Bestandebene aus.

Sie können die Schaltfläche **Produkte aktualisieren** im Aktionsbereich auswählen, um den Wert des Profils auf Kategorieebene an die zugrunde liegenden Produkte der Kategorie weiterzugeben. Weitere Informationen finden Sie unter [Produktkategorien und Produkte verwalten](category-management-product-creation.md).

Um ein Lagerbestandsprofil für ein Produkt freizugeben, folgen Sie diesen Schritten.

1. Navigieren Sie zu **Einzelhandel und Handel** \> **Produkte und Kategorien** \> **Freigegebene Produkte nach Kategorie**.
1. Wählen Sie ein Produkt aus und öffnen Sie die Produktdetailseite.
1. Im Inforegister **Verkauf** im Abschnitt **Commerce Bestand** im Feld **Profil auf Bestandebene** wählen Sie im Feld eines der vordefinierten Profile auf der Bestandebene aus.

Wenn ein neues Produkt erstellt wird, wird das Feld **Profil auf Inventarebene** wie viele andere Attribute auf Produktebene auf den Wert gesetzt, der für die Kategorie konfiguriert ist, der das Produkt zugeordnet ist.

> [!NOTE]
> Das Inventarebenenprofil ist ein für eine juristische Person spezifisches Attribut. Für dieselbe Kategorie oder dasselbe Produkt kann der Profilwert auf Inventarebene zwischen juristischen Personen variieren.

Führen Sie die folgenden Schritte aus, um die Konfigurationen von Profilen auf Inventarebene mit Kanälen zu synchronisieren.

1. Gehen Sie zu **Retail and Commerce** \> **Retail and Commerce IT** \> **Vertriebsplan**.
1. Führen Sie den Verteilungsplan **1040** (**Produkt**) aus.

## <a name="configure-an-inventory-buffer"></a>Konfigurieren Sie einen Inventarpuffer

Der *Inventarpuffer* ist ein benutzerdefinierter Wert, der die zusätzliche Menge eines Artikels von der ursprünglichen Menge subtrahiert, um die geschätzte Menge zu berechnen. Diese geschätzte Menge bietet Einzelhändlern einen sicheren Puffer, damit sie ein Produkt nicht überbieten, indem sie mehr als den tatsächlichen Lagerbestand verkaufen. Sie können das Inventarebenenprofil entweder auf Produktkategorieebene oder auf der Ebene der einzelnen Produkte konfigurieren. Wenn kein Bestandpuffer angegeben wird, wird der Wert **0** (Null) verwendet.

Um den Lagerbestandpuffer für eine Kategorie zu konfigurier, folgen Sie diesen Schritten.

1. Gehen Sie zu **Retail and Commerce** \> **Produkte und Kategorien** \> **Commerce-Produkthierarchie**.
1. Wählen Sie die Kategorie, um den Bestandpuffer zu konfigurieren.
1. Auf dem Inforegister **Verkaufen Sie Produkteigenschaften** wählen Sie eine juristische Person aus.
1. In dem Abschnitt **Commerce Bestand** im Feld **Bestandpuffer** geben Sie im Feld einen positiven Wert ein.

Sie können die Schaltfläche **Produkte aktualisieren** im Aktionsbereich auswählen, um den Wert des Puffers auf Kategorieebene an die zugrunde liegenden Produkte der Kategorie weiterzugeben. Weitere Informationen finden Sie unter [Produktkategorien und Produkte verwalten](category-management-product-creation.md).

Um den Lagerbestandpuffer für ein freigegebene Produkt zu konfigurieren, folgen Sie diesen Schritten.

1. Navigieren Sie zu **Einzelhandel und Handel** \> **Produkte und Kategorien** \> **Freigegebene Produkte nach Kategorie**.
1. Wählen Sie ein Produkt aus und öffnen Sie die Produktdetailseite.
1. In Inforegister **Verkaufen** i Abschnitt **Commerce Bestand** im Feld **Bestandpuffer** geben Sie im Feld einen positiven Wert ein.

Wenn ein neues Produkt erstellt wird, wird das Feld **Bestandpuffer** wie viele andere Attribute auf Produktebene auf den Wert gesetzt, der für die Kategorie konfiguriert ist, der das Produkt zugeordnet ist.

> [!NOTE]
> Wenn sowohl das Inventarpuffer- als auch das Inventarebenenprofil für ein Produkt konfiguriert sind, wird die geschätzte Menge des Produkts (dh die ursprüngliche Menge abzüglich des Pufferwerts) für die Bereichsberechnung verwendet, um den Inventarbestand zu bestimmen.

Führen Sie die folgenden Schritte aus, um die Konfigurationen von Bestandpuffern mit Kanälen zu synchronisieren.

1. Gehen Sie zu **Retail and Commerce** \> **Retail and Commerce IT** \> **Vertriebsplan**.
1. Führen Sie den Verteilungsplan **1040** (**Produkt**) aus.

## <a name="use-inventory-buffers-and-inventory-levels-in-e-commerce-scenario"></a>Verwenden Sie Bestandpuffer und Bestandebenen im E-Commerce-Szenario

Der Commerce Site Builder verwendet die Funktionen für den Bestandpuffer und die Bestandebene in der Commerce-Zentrale, um die Nachrichten zur Verfügbarkeit des Inventars auf E-Commerce-Sites zu ermitteln. Weitere Informationen finden Sie unter [Bestandeinstellungen anwenden](inventory-settings.md).

Wenn Sie eine E-Commerce-Lösung eines Drittanbieters integrieren, können Sie alternativ die **GetEstimatedAvailability** und **GetEstimatedProductWarehouseAvailability** APIs zur Anzeige der Inventarverfügbarkeit für ein Produkt in Ihrem E-Commerce-Szenario verwenden. Weitere Informationen zu diesen APIs finden Sie unter [Berechnen Sie die Bestandverfügbarkeit für Retail Channel](calculated-inventory-retail-channels.md).

Durch die Einführung von Bestandpuffern und Bestandebenen können diese APIs Codes für Bestandebenen und Kennzeichnungsnachrichten zurückgeben, die auf der Grundlage der insgesamt verfügbaren und verfügbaren physischen Werte ermittelt werden. Die APIs können weiter konfiguriert werden, um zu bestimmen, ob die Bestandmenge zusammen mit der Nachricht zurückgegeben wird und ob die verfügbare Menge um den Bestandpufferwert reduziert wird.

Führen Sie die folgenden Schritte aus, um die Antwort der Produktverfügbarkeits-APIs zu konfigurieren.

1. Gehen Sie zu **Retail and Commerce** \> **Heaquaters einrichten** \> **Parameter** \> **Commerce-Parameter**.
1. In dem **Inventar speichern** Abschnitt, auf der **Inventar** Registerkarte im Feld **Produktverfügbarkeits-APIs für E-Commerce** wählen Sie einen Wert.
1. Um die Einstellungen auf Kanäle anzuwenden, führen Sie den **1110** (**Globale Konfiguration**) Verteilungsplanjob aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Produktkategorien und Produkte verwalten](category-management-product-creation.md)

[Wenden Sie Inventareinstellungen an](inventory-settings.md)

[Lagerverfügbarkeit für Retail Channels berechnen](calculated-inventory-retail-channels.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
