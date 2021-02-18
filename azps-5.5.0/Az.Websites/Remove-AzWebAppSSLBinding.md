---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100253400"
---
# Remove-AzWebAppSSLBinding

## SYNOPSIS
Tar bort en SSL-bindning från ett uppladdat certifikat.

## SYNTAX

### S1
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Remove-AzWebAppSSLBinding** tar bort en SSL-bindning (SSL (Secure Sockets Layer)) från en Azure Web App.
SSL-bindningar används för att associera en Web App med ett certifikat.

## EXEMPEL

### Exempel 1: Ta bort en SSL-bindning för en webbapp
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Det här kommandot tar bort SSL-bindningen för webbappen ContosoWebApp.
Eftersom *parametern DeleteCertificate* inte ingår tas certifikatet bort om det inte längre har NÅGRA SSL-bindningar.

### Exempel 2: Ta bort en SSL-bindning utan att ta bort certifikatet
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Precis som i exempel 1 tar det här kommandot även bort SSL-bindningen för Web App ContosoWebApp.
I det här fallet ingår *dock parametern DeleteCertificate* och parametervärdet anges till $False.
Det innebär att certifikatet inte kommer att tas bort oavsett om det har SSL-bindningar eller inte.

### Exempel 3: Använda en objektreferens för att ta bort en SSL-bindning
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

I det här exemplet används en objektreferens till Web App-webbplatsen för att ta bort SSL-bindningen för en Web App.
Det första kommandot använder cmdleten Get-AzWebApp skapa en objektreferens till webbappen ContosoWebApp.
Objektreferensen lagras i en variabel med namnet $WebApp.
Det andra kommandot använder objektreferensen och **cmdleten Remove-AzWebAppSSLBinding** för att ta bort SSL-bindningen.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeleteCertificate
Anger vilken åtgärd som ska vidtas om SSL-bindningen tas bort är den enda bindningen som används av certifikatet.
Om *DeleteCertificate* är $False tas inte certifikatet bort när bindningen tas bort.
Om *DeleteCertificate* är inställt på $True eller inte ingår i kommandot tas certifikatet bort tillsammans med SSL-bindningen.
Certifikatet tas bara bort om SSL-bindningen tas bort är den enda bindningen som används av certifikatet.
Om certifikatet har mer än en bindning tas certifikatet inte bort oavsett värdet för *parametern DeleteCertificate.*

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Tvingar kommandot att köras utan att användaren uppmanas att bekräfta.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Anger namnet på webbappen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resursgrupp som certifikatet är tilldelat till.
Du kan inte använda *parametern ResourceGroupName* och *WebApp* i samma kommando.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Anger distributionsplats för Web App.
Om du vill skaffa en distributionsplatsen använder du Get-AzWebAppSlot-cmdleten.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Anger en webbapp.
Om du vill skaffa en webbapp använder du Get-AzWebApp-cmdleten.
Du kan inte använda *WebApp-parametern* i samma kommando som *ResourceGroupName-parametern* och/eller *WebAppName.*

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Anger namnet på webbappen.
Du kan inte använda *WebAppName-parametern* *och WebApp-parametern* i samma kommando.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte. Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## UTDATA

### System.Void

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzWebAppsSLBinding](./Get-AzWebAppSSLBinding.md)

[New-AzWebAppsSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


