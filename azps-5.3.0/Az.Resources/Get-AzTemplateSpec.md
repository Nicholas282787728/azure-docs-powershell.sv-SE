---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521476"
---
# Get-AzTemplateSpec

## Sammanfattning
Hämtar eller visar mallens specifikationer

## FRÅGESYNTAXEN

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

## PROBLEMBESKRIVNING
Denna cmdlet kan användas för att ange listmallar i en prenumeration/resurs grupp eller för att få en specifik mall med namn eller ID. När du får en specifik mall genom att ange namn/ID för en specifik version kan du välja att hämta ett versions namn via parametern **-version** . När **-version** används visas bara den specifika versions informationen i **. Versioner* av spec-objektet för den returnerade mallen. Om du inte har angett någon specifik version när du hämtar en mall specifikation via namn/ID finns alla versioner i **. Egenskapen versions* för det returnerade objektet.

**Obs!** när du visar en lista med alla specifikationer för mallar i en prenumeration eller resurs grupp visas en specifikation för varje mall som returnerar *". Versions* värden är *Null*. Versions information ingår endast när-namn-eller-ResourceId-parametrar tillhandahålls (tex: du begär en specifik mall specifikation/version).

## BESKRIVS

### Exempel 1: specifikationer för listmall i aktuell prenumeration
```powershell
PS C:\> Get-AzTemplateSpec
```

Här listas alla specifikationer för mallar i det aktuella abonnemanget.

### Exempel 2: specifikationer för listmall i en resurs grupp
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Visar alla mallalternativ i resurs gruppen ' myRG ' för det aktuella abonnemanget.

### Exempel 3: Hämta mall-specifikation (med alla versioner) efter namn
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Hämtar information om mallnamnet "MyTemplateSpec" i resurs gruppen "myRG".

**Obs!** alla specifikationer för mallar finns i "*. Versioner*"-egenskapen för returvärdet.

### Exempel 4: Hämta specifikation (specifik version) efter namn
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Hämtar information om version ' v 1.0 ' för mallnamnet med namnet "MyTemplateSpec" i resurs gruppen "myRG".

**Obs!** *". Versioner "* egenskapen för det returnerade objektet innehåller endast den begärda versionen.

### Exempel 5: Hämta mall-specifikation (med alla versioner) efter resurs-ID
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Hämtar information om mallnamnet "MyTemplateSpec" i resurs gruppen "myRG" för prenumerations \{ subId \} .

**Obs!** alla specifikationer för mallar finns i "*. Versioner*"-egenskapen för returvärdet.

### Exempel 6: Hämta mallens spec (specifik version) efter resurs-ID
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Hämtar information om version ' v 1.0 ' för mallnamnet med namnet "MyTemplateSpec" i resurs gruppen "myRG" för abonnemanget \{ subId \} .

**Obs!** *". Versioner "* egenskapen för det returnerade objektet innehåller endast den begärda versionen.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -Namn
Namnet på mallens spec.

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
Namnet på resurs gruppen.

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
Fullständigt resurs-ID för mallens spec. exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

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
Versionen av mallens spec.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSTemplateSpec

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
