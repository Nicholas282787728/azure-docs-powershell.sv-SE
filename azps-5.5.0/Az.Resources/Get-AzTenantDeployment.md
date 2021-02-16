---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226831"
---
# Get-AzTenantDeployment

## SYNOPSIS
Distribuera på klientorganisationens omfattning

## SYNTAX

### GetByDeploymentName (standard)
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzTenantDeployment** hämtar distributionerna på klientorganisationens omfattning.
Ange *namn- eller* *Id-parametern* för att filtrera resultatet.
Som standard **hämtar Get-AzTenantDeployment** alla distributioner på klientorganisationens omfattning.

## EXEMPEL

### Exempel 1: Hämta alla distributioner i klientorganisationens omfattning
```
PS C:\>Get-AzTenantDeployment
```

Det här kommandot hämtar alla distributioner på den aktuella klientorganisationens omfattning.

### Exempel 2: Hämta en distribution efter namn
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

Det här kommandot får distributionen "Distribuera01" på den aktuella klientorganisationens omfattning.
Du kan tilldela en distribution ett namn när du skapar den med cmdletsna **New-AzTenantDeployment.**
Om du inte tilldelar ett namn tillhandahåller cmdletarna ett standardnamn baserat på mallen som används för att skapa distributionen.

### Exempel 3: Hämta en distribution med ID
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

Det här kommandot får distributionen "Distribuera01" i klientorganisationens omfattning.

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

### -Id
Det fullständigt kvalificerade resurs-ID:t för distributionen.
exempel: /providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Namnet på distributionen.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
När detta anges anger det att cmdleten ska använda förhandsversioner av API-versioner när det automatiskt avgör vilken version som ska användas.

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDutbetalning

## ANTECKNINGAR

## RELATERADE LÄNKAR
