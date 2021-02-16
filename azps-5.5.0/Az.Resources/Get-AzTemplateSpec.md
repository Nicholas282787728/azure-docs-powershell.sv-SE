---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226846"
---
# Get-AzTemplateSpec

## SYNOPSIS
Hämtar eller listar mallspecifikter

## SYNTAX

### ListTemplateSpecsParameterSet (standard)
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetTemplateSpecByNameParameterSet
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetTemplateSpecByIdParameterSet
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Den här cmdleten kan användas för att lista mallspecifikter i en prenumeration/resursgrupp eller få en specifik mallspecifikation efter namn eller id. När du hämtar en specifik mallspecifiktör med namn/id kan du välja att hämta en viss version genom att ange ett versionsnamn via **parametern -Version.** När **-Version** används finns endast den specifika versionsinformationen i **. Versioner* av det returnerade mallspecifikt objektet. Om ingen specifik version anges när du hämtar en mallspecifikt efter namn/id finns alla versioner i **. Egenskapen* Versioner för det returnerade objektet.

**Obs!** När alla mallspecifikter listas i en prenumeration eller resursgrupp returneras "." *Versionsegenskapen* blir *null.* Versionsinformation ingår endast när -Name eller -ResourceId-parametrar tillhandahålls (t.ex. du begär en specifik mallspecifik/version).

## EXEMPEL

### Exempel 1: Listmallsspecifikation i aktuell prenumeration
```powershell
PS C:\> Get-AzTemplateSpec
```

Visar alla mallspecifikationerna i den aktuella prenumerationen.

### Exempel 2: Listmallsspecifikter i en resursgrupp
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Visar alla mallspecifikter i resursgruppen "myRG" för den aktuella prenumerationen.

### Exempel 3: Hämta mallspecifikt (med alla versioner) efter namn
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Hämtar information om mallspecifikt "MyTemplateSpec" i resursgruppen "myRG".

**Obs!** Alla versioner av mallspecifikt finns i "*.* Versionsegenskapen för det returnerade objektet.

### Exempel 4: Hämta mallspecifikt (specifik version) efter namn
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Hämtar information om version "v1.0" av mallspecifikt "MyTemplateSpec" i resursgruppen "myRG".

**Obs!** *". Egenskapen Versioner"* för det returnerade objektet innehåller endast den specifika version som begärs.

### Exempel 5: Hämta mallspecifikt (med alla versioner) efter resurs-ID
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Hämtar information om mallspecifikationen med namnet MyTemplateSpec inom resursgruppen "myRG" i \{ prenumerationsunderid. \}

**Obs!** Alla versioner av mallspecifikt finns i "*.* Versionsegenskapen för det returnerade objektet.

### Exempel 6: Hämta mallspecifikt (specifik version) efter resurs-ID
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Hämtar information om version "v1.0" av mallspecifikationen med namnet "MyTemplateSpec" inom resursgruppen "myRG" av \{ prenumerationsunder-ID. \}

**Obs!** *". Egenskapen Versioner"* för det returnerade objektet innehåller endast den specifika version som begärs.

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

### -Name
Namnet på mallspecifikt.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resursgruppen.

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Fullständigt kvalificerat resurs-ID för mallspecifikationer. Exempel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Versionen av mallspecifikt.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.ResourceManager.cmdlets.SdkModels.PSTemplateSpec

## ANTECKNINGAR

## RELATERADE LÄNKAR
