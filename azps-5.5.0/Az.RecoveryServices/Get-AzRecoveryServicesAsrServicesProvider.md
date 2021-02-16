---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 5ede0387f5aabb1a4f4c4814f8090e0feeda2bf2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227071"
---
# Get-AzRecoveryServicesAsrServicesProvider

## SYNOPSIS
Hämtar information om ASR-leverantörer av återställningstjänster som är registrerade i valv för Återställningstjänster.

## SYNTAX

### Standard (standard)
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByName
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzRecoveryServicesAsrServicesProvider** hämtar information på Azure-webbplatsåterställningsleverantörerna i valvet.

## EXEMPEL

### Exempel 1
```powershell
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

Lista alla ASR-replikeringstjänster som är registrerade på Recovery Services-valvet som motsvarar den angivna strukturen.

### Exempel 2

Hämtar information om ASR-leverantörer av återställningstjänster som är registrerade i valv för Återställningstjänster. (autogenererat)

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesAsrServicesProvider -Fabric $Fabric
```

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.


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

### -Fabric
Anger ASR-strukturobjektet.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -FriendlyName
Anger eget namn på tjänstleverantören för ASR-återställningstjänster som du vill få information om.

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Anger namnet på asr-återställningstjänster som du vill få information om.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric

## UTDATA

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Remove-AzRecoveryServicesAsrServicesProvider](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[Update-AzRecoveryServicesAsrServicesProvider](./Update-AzRecoveryServicesAsrServicesProvider.md)
