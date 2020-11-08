---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093359"
---
# Get-AzurePublishSettingsFile

## Sammanfattning
Laddar ned filen för publicerings inställningar för en Azure-prenumeration.

## FRÅGESYNTAXEN

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzurePublishSettingsFile** laddar ned en fil för publicerings inställningar för en prenumeration på ditt konto.
När kommandot är klart kan du använda cmdleten **import-PublishSettingsFile** för att göra inställningarna i filen tillgängliga för Windows PowerShell.

Om du vill göra ditt Azure-konto tillgängligt för Windows PowerShell kan du använda en fil för publicerings inställningar eller cmdleten **Add-AzureAccount** .
Med publicerings inställningar kan du förbereda sessionen i förväg så att skript och bakgrunds jobb inte körs.
Men alla tjänster stöder inte publicerings inställningar.
**AzureResourceManager** -modulen stöder till exempel inte publicerings inställningar.

När du kör **Get-AzurePublishSettingsFile** öppnas standard webbläsaren och du uppmanas att logga in på ditt Azure-konto, välja ett abonnemang och välja en plats för fil system för publicerings inställnings filen.
Sedan hämtas filen för publicerings inställningar för ditt abonnemang till den valda filen.

En "publicerings inställnings fil" är en XML-fil med fil namns tillägget. publishsettings.
Filen innehåller ett kodat certifikat som innehåller administratörsautentiseringsuppgifter för dina Azure-prenumerationer.

**Säkerhets meddelande:** Publicering Settings innehåller autentiseringsuppgifter som används för att administrera dina Azure-abonnemang och-tjänster.
Om illvilliga användare kommer åt filen för publicerings inställningar kan de redigera, skapa och ta bort dina Azure-tjänster.
Av säkerhets skäl bör du spara filen på en plats i mappen Hämtade filer eller dokument och sedan ta bort den när du har använt cmdleten **import-AzurePublishSettingsFile** för att importera inställningarna.

I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

## BESKRIVS

### Exempel 1: Ladda ned en fil för publicerings inställningar
```
PS C:\> Get-AzurePublishSettingsFile
```

Det här kommandot öppnar standard webbläsaren, ansluter till ditt Windows Azure-konto och laddar sedan ned. publishsettings-filen för ditt konto.

### Exempel 2: Ange en sfär
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

Det här kommandot laddar ned filen för publicerings inställningar för ett konto i contoso.com-domänen.
Använd ett kommando med parametern **Realm** när du loggar in på Azure med ett organisations konto i stället för ett Microsoft-konto.

## MALLPARAMETRAR

### -Miljö
Anger en Azure-miljö.

En Azure-miljö en oberoende distribution av Microsoft Azure, till exempel AzureCloud för globala Azure-och AzureChinaCloud för Azure som drivs av 21Vianet i Kina.
Du kan också skapa lokala Azure-miljöer med Azure Pack och WAPack cmdlets.
Mer information finns i [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Returnerar $True om kommandot lyckas och $False om det inte fungerar.
Denna cmdlet returnerar som standard inga utdata.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser. Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Realm
Anger organisationen i ett organisations-ID.
Om du till exempel loggar in på Azure as admin@contoso.com är värdet för parametern **Realm** contoso.com.
Använd den här parametern när du loggar in på Azure-portalen med ett organisations-ID.
Denna parameter behövs inte när du använder ett Microsoft-konto, till exempel ett outlook.com-eller live.com-konto.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.

## VÄRDEN

### Ingen eller system. Boolean
När du använder parametern *Passthru* returnerar denna cmdlet ett Boolean-värde.
Annars returnerar denna cmdlet inte något utdata

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureAccount](./Add-AzureAccount.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)


