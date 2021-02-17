---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: c22643c4ce47fc59d2640a6dbbdf9c15b0846f98
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212926"
---
# Get-AzADSpCredential

## SYNOPSIS
Hämtar en lista med autentiseringsuppgifter som är kopplade till en tjänsts huvudnamn.

## SYNTAX

### ObjectIdParameterSet (standard)
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNObjectParameterSet
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Den Get-AzADSpCredential cmdleten kan användas för att hämta en lista med autentiseringsuppgifter som är kopplade till en tjänsts huvudnamn.
Med det här kommandot hämtas alla autentiseringsegenskaper (men inte autentiseringsvärdet) som är kopplade till tjänstens huvudnamn.

## EXEMPEL

### Exempel 1 : Listautentiseringsuppgifter efter SPN

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

Returnerar en lista med autentiseringsuppgifter som är kopplade till tjänstens huvudnamn med SPN http://test12345 ' '.

### Exempel 2 : Lista autentiseringsuppgifter efter objekt-ID

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

Returnerar en lista med autentiseringsuppgifter som är associerade med tjänstens huvudnamn med objekt-ID "58e28616-99cc-4da4-b705-7672130e1047".

### Exempel 3 : Lista autentiseringsuppgifter genom rörning

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

Hämtar tjänstens huvudnamn med objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" och rör den till Get-AzADSpCredential-cmdleten för att visa alla autentiseringsuppgifter för tjänstens huvudnamn.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

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

### -DisplayName
Tjänstens huvudnamn

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Objekt-ID för den tjänsts huvudnamn som autentiseringsuppgifterna ska hämtas från.

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Namnet (SPN) på tjänstens huvudnamn som autentiseringsuppgifterna ska hämtas från.

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalObject
Det huvudobjekt för tjänsten som autentiseringsuppgifterna ska hämtas från.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal

## UTDATA

### Microsoft.Azure.Commands.ActiveDirectory.PSADCredential

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

