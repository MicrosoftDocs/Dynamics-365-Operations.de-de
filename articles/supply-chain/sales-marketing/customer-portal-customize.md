---
title: Debitorenportal anpassen und verwenden
description: In diesem Artikel wird erläutert, wie Sie das Kundenportal anpassen, nachdem es Ihrem System hinzugefügt wurde.
author: Henrikan
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 85ec4beda2efe62ff5076a5ed694efbc47c6d87f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878873"
---
# <a name="customize-and-use-the-customer-portal"></a>Debitorenportal anpassen und verwenden

[!include [banner](../includes/banner.md)]


In diesem Artikel werden die verschiedenen Seiten beschrieben, die im Kundenportal sofort verfügbar sind. Es wird erklärt, was die Seiten tun und wie Sie sie anpassen können.

Das Kundenportal bietet einige vordefinierte Websiten und Aktionen. Die folgende Sitemap bietet einen Überblick über diese Webseiten und Aktionen sowie die Rollen, die die Aktionen ausführen können.

![Kundenportal-Sitemap.](media/customer-portal-site-map.png "Kundenportal-Sitemap")

## <a name="typical-customizations"></a>Typische Anpassungen

Die folgenden Artikel helfen Ihnen beim Erlernen der Grundlagen von Power Apps Portal und wie Sie Portale anpassen können:

- [Arbeiten Sie mit Vorlagen](/powerapps/maker/portals/work-with-templates) – Dieser Artikel bietet einen allgemeinen Überblick darüber, wie Power Apps Portale funktionieren und wie Sie einfache Anpassungen von Portalen vornehmen können.
- [Portalinhalte verwalten](/dynamics365/portals/manage-portal-content) – In diesem Artikel wird erläutert, wie Sie den Inhalt verwalten und anpassen können, den Sie in Ihrem Portal anzeigen.
- [Bearbeiten von CSS](/powerapps/maker/portals/edit-css) – Mit diesem Artikel können Sie komplexere Anpassungen an der Benutzeroberfläche Ihres Portals vornehmen.
- [Erstellen Sie ein Thema für Ihr Portal](/dynamics365/portals/create-theme) – Mit diesem Artikel können Sie ein UI-Thema für Ihr Portal erstellen.
- [Erstellen und Anzeigen von Portalinhalten auf einfache Weise](/dynamics365/portals/create-expose-portal-content) – In diesem Artikel können Sie die zugrunde liegenden Daten und Tabellen verwalten, die Sie für Ihr Portal verwenden.
- [Konfigurieren Sie einen Kontakt für die Verwendung in einem Portal](/powerapps/maker/portals/configure/configure-contacts) – In diesem Artikel wird erläutert, wie Benutzerrollen erstellt und angepasst werden und wie Sicherheit und Authentifizierung in Power Apps Portalen funktionieren.
- [Konfigurieren Sie Notizen für Tabellenformulare und Webformulare auf Portalen](/powerapps/maker/portals/configure-notes) – In diesem Artikel wird erläutert, wie Sie Ihrem Portal Dokumente und zusätzlichen Speicher hinzufügen.
- [Fehlerbehandlung für Portal-Website](/powerapps/maker/portals/admin/view-portal-error-log) – In diesem Artikel wird erläutert, wie Sie Portalfehlerprotokolle anzeigen und in I Microsoft Azure Blob-Speicherkonto speichern.

## <a name="customize-the-order-creation-process"></a>Passen Sie den Prozess der Auftragserstellung an

Wenn ein Benutzer eine Bestellung über das Kundenportal abgibt, wird die Bestellung automatisch mit der entsprechenden Dynamics 365 Supply Chain Management Umgebung synchronisiert. Da der Benutzer ein externer Kunde ist, werden gewisse erforderliche Informationen absichtlich vor ihm verborgen. Diese Informationen werden automatisch ausgefüllt, wenn das Formular gesendet wird.

Dieser Abschnitt zeigt, wie Sie Kontakte einrichten sollten, um Fehler zu vermeiden. Es werden Felder erläutert, die automatisch festgelegt werden, und wie Sie den Wert dieser Felder bei Bedarf ändern können.

### <a name="the-out-of-box-order-creation-process"></a>Definierten Prozess der Auftragserstellung anpassen

Hier sind die Standardschritte zum Absenden eines Auftrags über das Kundenportal.

1. Wählen Sie auf der Startseite die Kachel **Auftrag erstellen** zum Öffnen des Assistenten **Auftrag erstellen**.
1. Auf der Seite **Bestellinformationen** setzen Sie die folgenden Felder fest:

    - **Angefordertes Empfangsdatum** – Geben Sie das Lieferdatum an.
    - **Lieferadresse** – Geben Sie die Adresse ein, an die die Bestellung geliefert werden soll.
    - **Unternehmen** – Wählen Sie den Namen des Kundenunternehmens. Dieses Feld wird automatisch für Benutzer ohne Administratorrechte festgelegt.
    - **Anforderungsnummer** – Geben Sie die Bestellnummer der Bestellung ein. Dieses Feld ist nicht erforderlich.
    - **Versand nach Land/Region** – Geben Sie das Land oder die Region ein, in die die Artikel geliefert werden sollen. Dieses Feld wird automatisch für Benutzer ohne Administratorrechte festgelegt.

    ![Auftragsinformationsseite.](media/customer-portal-order-information.png "Auftragsinformationsseite")

1. Wählen Sie **Weiter**.
1. Wählen Sie auf der Seite **Artiekl** **Artikel hinzufügen** aus.

    ![Artikelseite.](media/customer-portal-items.png "Artikelseite")

1. Im angezeigten Dialogfeld **Artikelinformation** legen Sie die folgenden Felder fest:

    - **Produktname** – Suchen Sie ein Produkt und wählen Sie es aus, um es der Bestellung hinzuzufügen.
    - **Menge** – Geben Sie die Menge des ausgewählten Produkts an.
    - **Einheit** – Geben Sie die Maßeinheit an (z. B. **ea.**, **kg**, oder **Schachtel**).
    - **Geschätzter Nettobetrag** – Der Wert wird berechnet als der geschätzte Preis des Artikels × die Menge für die ausgewählte Einheit.

    ![Dialogfeld Artikelinformation.](media/customer-portal-item-information.png "Dialogfeld Artikelinformation")

1. Wählen Sie **Übermitteln**, um dem Auftrag den Artikel hinzuzufügen.
1. Wiederholen Sie die Schritte 4 bis 6, bis Sie alle Artikel hinzugefügt haben, die Sie bestellen möchten.
1. Wenn Sie alle Elemente hinzugefügt haben, wählen Sie **Weiter** auf der Seite **Artikel**.
1. Die Seite **Bestellinformationen** zeigt eine Zusammenfassung der Bestellung. Überprüfen Sie den Bestellinhalt und die Lieferdetails. Wenn alles richtig aussieht, wählen Sie **übermitteln**, um die Bestellung abzuschicken.

    ![Abgeschlossene Auftragsinformationsseite.](media/customer-portal-order-submit.png "Abgeschlossene Auftragsinformationsseite")

### <a name="standard-data-setup"></a>Standarddaten einrichten

Um eine reibungslose Benutzererfahrung zu gewährleisten, füllt das Kundenportal automatisch Werte für mehrere erforderliche Felder aus. Diese Werte basieren auf Informationen im Kontaktdatensatz des Kunden, der die Bestellung abgibt.

Für jede [Kontaktzeile](/powerapps/maker/portals/configure/configure-contacts), die zu einem Kunden gehört, der das Kundenportal zum Absenden von Bestellungen verwendet, müssen für die folgenden erforderlichen Felder Werte angegeben werden. Andernfalls treten Fehler auf.

- **Unternehmen** – Die juristische Person, zu der der Auftrag gehört
- **Möglicher Kunde** – Das dem ausgewählten Auftrag zugeordnete Debitorenkonto
- **Preisliste** – Die benutzerdefinierte Preisliste für den Kunden
- **Währung** – Die Währung des Preises
- **Versand nach Land/Region** – Das Land oder die Region eingeben, in die die Artikel geliefert werden sollen

Die folgenden Felder werden automatisch für die Auftragstabelle festgelegt:

- **Sprache** – Die Sprache der Bestellung (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)
- **Versand nach Land/Region** – Das Land oder die Region, in die die Artikel geliefert werden (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)
- **Kontaktperson** – Der Benutzer, der kontaktiert werden kann, um Informationen zur Bestellung zu erhalten (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)
- **Unternehmen** – Die juristische Person, zu der die Bestellung gehört (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)
- **Potenzieller Kunde** – Das Kundenkonto, das der Bestellung zugeordnet ist (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)
- **Kundenrechnung** – Das Kundenkonto, das der Bestellung zugeordnet ist (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)
- **Kundenauftragsname** – Der Name des Kundenauftrags (Der Standardwert ist **Kundenauftrag** .)
- **Währung** – Die Währung des Preises (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)
- **Preisliste** – Die benutzerdefinierte Preisliste für den Kunden (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)
- **Beschreibung der Lieferadresse** – Die Lieferadresse des Kundenauftrags (Der Standardwert ist **Beschreibung der Lieferadresse** .)

### <a name="modify-the-order-creation-process"></a>Den Prozess der Auftragserstellung anpassen

Sie können das Erscheinungsbild und die Benutzeroberfläche des Kundenportals frei ändern, wenn Sie den grundlegenden Prozess zur Auftragserstellung nicht ändern. Wenn Sie den Prozess der Auftragserstellung ändern möchten, müssen Sie einige Punkte beachten.

Entfernen Sie die folgenden Spalten nicht aus der Auftragstabelle in Microsoft Dataverse, weil sie einen Auftrag in dualem Schreiben erstellen müssen:

- **Unternehmen** – Die juristische Person, zu der der Auftrag gehört
- **Name** –Der Name des konsolidierten Verkaufsauftrags
- **Währung** – Die Währung des Preises
- **Preisliste** – Die benutzerdefinierte Preisliste für den Kunden
- **Versand nach Land/Region** – Das Land oder die Region eingeben, in die die Artikel geliefert werden sollen
- **Möglicher Kunde** – Das dem ausgewählten Auftrag zugeordnete Debitorenkonto
- **Sprache** – Die Sprache der Bestellung (In der Regel ist diese Sprache die Sprache des potenziellen Kunden.)
- **Beschreibung der Lieferadresse** – Die Lieferadresse des Kundenauftrags

Für Artikel sind folgende Spalten erforderlich:

- **Produkt** – Das zu bestellende Produkt
- **Menge** – Die Menge des ausgewählten Produkts
- **Einheit** – Die Maßeinheit (z. B. **ea.**, **kg**, oder **Schachtel**)
- **Versand nach Land/Region** – Das Land oder die Region der Lieferung
- **Beschreibung der Lieferadresse** – Die Lieferadresse des Kundenauftrags

Sie müssen sicherstellen, dass Ihr Kundenportal irgendwie Werte für alle diese Spalten übermittelt.

Wenn Sie der Seite Spalten hinzufügen oder Spalten entfernen möchten, lesen Sie [Erstellen oder Bearbeiten von Schnellerstellungsformularen für eine optimierte Dateneingabeerfahrung](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).

Wenn Sie ändern möchten, wie Spalten voreingestellt sind und wie Werte beim Speichern der Seite festgelegt werden, lesen Sie die folgenden Informationen in der Dokumentation Power Apps Portal:

- [Feld vorausfüllen](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [Wert beim Speichern festlegen](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>Passen Sie die Startseite an

Alle Steuerelemente im Kundenportal sind integrierte Power Apps Portal Steuerelemente. Sie können sie anpassen, indem Sie die folgenden Schritte ausführen [Verfassen Sie eine Seite](/powerapps/maker/portals/compose-page) in der Dokumentation Power Apps Portal.

Das einzige benutzerdefinierte Steuerelement, das in der Kundenportalvorlage enthalten ist, wird zum Erstellen der Kacheln auf der Startseite verwendet.

![Kacheln auf der Startseite.](media/customer-portal-home-page-tiles.png "Kacheln auf der Startseite")

Um die Kacheln auszuführen, führen Sie folgende Schritte aus.

1. Öffnen Sie die [Portal Management App](/powerapps/maker/portals/configure/configure-portal).
1. Wählen Sie im linken Navigationsbereich **Seitenvorlage** aus.

    ![Navigationsbereich der Portalverwaltung.](media/customer-portal-nav.png "Navigationsbereich der Portalverwaltung")

1. Wählen Sie die benannte Seitenvorlage aus **Startseite**.
1. Im Feld **Webvorlage** wählen Sie den Link **Startseite** aus, um den Quellcode für diese Seite zu öffnen.

    ![Webvorlagenfeld.](media/customer-portal-web-template.png "Webvorlagenfeld")

1. Sie sollten jetzt den gesamten Quellcode für die Homepage sehen und können ihn nach Bedarf ändern.

## <a name="resources"></a>Ressourcen

Weitere Informationen zum Einrichten und Anpassen des Kundenportals finden Sie in den folgenden Ressourcen:

- [Power Apps Portaldokumentation](/powerapps/maker/portals/overview)
- [Dokumentation Duales Schreiben](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [Informationen zum Portallebenszyklus](/powerapps/maker/portals/admin/portal-lifecycle)
- [Aktualisieren Sie ein Portal](/powerapps/maker/portals/admin/upgrade-portal)
- [Portalkonfiguration migrieren](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Solution Lifecycle Management: Dynamics 365 for Customer Engagement Apps](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]