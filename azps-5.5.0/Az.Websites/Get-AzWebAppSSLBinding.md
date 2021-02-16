---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: aaecb97932ffbd2d7f5a03e4eedebd47719c5b4f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252721"
---
# Get-AzWebAppSSLBinding

## SYNOPSIS
Får SSL-bindningen Azure Web App-certifikat.

## SYNTAX

### S1
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzWebAppSSLBinding** får en SSL-bindning (SSL (Secure Sockets Layer)) för en Azure Web App.
SSL-bindningar används för att associera en Web App med ett uppladdat certifikat.
Webbappar kan vara bundna till flera certifikat.

## EXEMPEL

### Exempel 1: Hämta SSL-bindningar för en webbapp
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

Det här kommandot hämtar SSL-bindningarna för Web App ContosoWebApp, som är kopplad till resursgruppen ContosoResourceGroup.

### Exempel 2: Använda en objektreferens för att hämta SSL-bindningar för en Web App
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

Kommandona i det här exemplet hämtar även SSL-bindningarna för Web App ContosoWebApp. I det här fallet används en objektreferens i stället för webbappens namn och namnet på den associerade resursgruppen.
Den här objektreferensen skapas av det första kommandot i exemplet, som använder **Get-AzWebApp** till att skapa en objektreferens till webbappen ContosoWebApp.
Objektreferensen lagras i en variabel med namnet $WebApp.
Den här variabeln, **och cmdleten Get-AzWebAppSSLBinding,** används sedan av det andra kommandot för att få SSL-bindningarna.

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

### -Name
Anger namnet på SSL-bindningen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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
Anger en Web App-distributionsplats.
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
Anger namnet på webbappen som den här cmdleten hämtar SSL-bindningar från.
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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## UTDATA

### Microsoft.Azure.Management.WebSites.Models.HostNameSslState

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzWebAppsSLBinding](./New-AzWebAppSSLBinding.md)

[Remove-AzWebAppsSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


