---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: 342ab551afdce144719d5ba49c25eb7559ba35a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755184"
---
# Remove-AzureRmADSpCredential

## Sammanfattning
Tar bort en autentiseringsuppgift från ett tjänst huvud.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ObjectIdWithKeyIdParameterSet (standard)
```
Remove-AzureRmADSpCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithKeyIdParameterSet
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyIdParameterSet
```
Remove-AzureRmADSpCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalObjectParameterSet
```
Remove-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Du kan använda Remove-AzureRmADSpCredential cmdlet för att ta bort en behörighets nycklar från ett säkerhets objekt om det rör sig om en kompromiss eller en del av förnyelsen av autentiseringsuppgiften.
Tjänstens huvud namn identifieras genom att ange antingen objekt-ID eller SPN (Service Principal Name).
Den autentiseringsuppgift som ska tas bort identifieras via dess tillhör ande ID om en enskild autentiseringsuppgift ska tas bort eller med en "alla"-växel för att ta bort alla autentiseringsuppgifter som är kopplade till tjänstens huvud objekt.

## BESKRIVS

### Exempel 1 – ta bort en specifik autentiseringsuppgift från ett SPN-namn

```
PS C:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

Tar bort autentiseringsuppgiften med ID ' 9044423a-60a3-45ac-9ab1-09534157ebb ' från tjänstens huvud namn med objekt-ID ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 '.

### Exempel 2 – ta bort alla autentiseringsuppgifter från ett huvud säkerhets objekt

```
PS C:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123
```

Tar bort alla autentiseringsuppgifter från tjänstens huvud konto med SPN " http://test123 ".

### Exempel 3 – ta bort alla autentiseringsuppgifter från ett tjänst huvud med ledning

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADSpCredential
```

Hämtar tjänstens huvud namn med objekt-ID ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' och pipes till Remove-AzureRmADSpCredential cmdlet för att ta bort alla autentiseringsuppgifter från den tjänstens huvud objekt.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Visnings namnet på tjänstens huvud konto.

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Växla till att ta bort autentiseringsuppgiften utan att bekräfta.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyId
Anger den autentiseringsinformation som ska tas bort.
Huvud-ID: na för ett tjänst huvud konto kan erhållas med hjälp av Get-AzureRmADSpCredential cmdlet.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Objekt-ID för tjänstens huvud namn som autentiseringsuppgifterna ska tas bort från.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Om du anger detta returneras sant om kommandot lyckades.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePrincipalName
Namnet (SPN) för tjänstens huvud namn som autentiseringsuppgifterna ska tas bort från.

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalObject
Tjänst huvud objekt som autentiseringsuppgifterna ska tas bort från.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. GUID

### System. String

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal
Parametrar: ServicePrincipalObject (ByValue)

## VÄRDEN

### System. Boolean

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmADSpCredential](./Get-AzureRmADSpCredential.md)

[New-AzureRmADSpCredential](./New-AzureRmADSpCredential.md)

[Get-AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

