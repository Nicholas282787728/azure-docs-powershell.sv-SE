---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 46ea58d66efbde588b1f7677477d3b7521b1d02c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575409"
---
# Remove-AzureRmWebAppSSLBinding

## Sammanfattning
Tar bort en SSL-bindning från ett uppladdat certifikat.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### S
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmWebAppSSLBinding** tar bort en SSL-bindning från en Azure Web App.
SSL-bindningar används för att koppla ett webb program till ett certifikat.

## BESKRIVS

### Exempel 1: ta bort en SSL-bindning för ett webb program
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Det här kommandot tar bort SSL-bindningen för webb programmet ContosoWebApp.
Eftersom parametern *DeleteCertificate* inte är inkluderad tas certifikatet bort om det inte längre har några SSL-bindningar.

### Exempel 2: ta bort en SSL-bindning utan att ta bort certifikatet
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Precis som i exempel 1 tar det här kommandot också bort SSL-bindningen för Web App-ContosoWebApp.
I det här fallet är parametern *DeleteCertificate* inkluderad och parametervärdet är inställt på $false.
Det innebär att certifikatet inte tas bort oavsett om det har SSL-bindningar eller inte.

### Exempel 3: använda en objekt referens för att ta bort en SSL-bindning
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

I det här exemplet används en objekt referens till Web App-webbplatsen för att ta bort SSL-bindningen för ett webb program.

Det första kommandot använder cmdleten Get-AzureRmWebApp för att skapa en objekt referens till webb programmet som heter ContosoWebApp.
Objekt referensen lagras i en variabel som heter $WebApp.

Det andra kommandot använder objekt referensen och cmdleten **Remove-AzureRmWebAppSSLBinding** för att ta bort SSL-bindningen.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeleteCertificate
Anger vilken åtgärd som ska vidtas om SSL-bindningen som tas bort är den enda bindning som används av certifikatet.
Om *DeleteCertificate* är inställt på $false tas certifikatet inte bort när bindningen tas bort.
Om *DeleteCertificate* är inställt på $True eller inte ingår i kommandot tas certifikatet bort tillsammans med SSL-bindningen.

Certifikatet tas bara bort om den SSL-bindning som tas bort är den enda bindning som används av certifikatet.
Om certifikatet har mer än en bindning tas certifikatet inte bort oavsett värdet på parametern *DeleteCertificate* .

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Tvingar kommandot att köras utan att fråga efter bekräftelse.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på webb programmet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen som certifikatet har tilldelats till.

Du kan inte använda parametern *ResourceGroupName* och *webapp* -parametern i samma kommando.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger webb programmets distributions plats.
Använd Get-AzureRMWebAppSlot cmdlet för att få en distributions plats.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Anger ett webb program.
Om du vill hämta en webbapp använder du Get-AzureRmWebApp cmdlet.

Du kan inte använda *webapp* -parametern i samma kommando som parametern *ResourceGroupName* och/eller *WebAppName*.

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Anger namnet på webb programmet.

Du kan inte använda parametern *WebAppName* och *webapp* -parametern i samma kommando.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte. Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Webbplatsmallar
Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)

[New-AzureRmWebAppSSLBinding](./New-AzureRmWebAppSSLBinding.md)

[Get-AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


