---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: e1da6e54eac3e72217e83e498966bdfa80740762
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212910"
---
# Get-AzDeploymentOperation

## SYNOPSIS
Hämta distributionsåtgärd

## SYNTAX

### GetByDeploymentName (standard)
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentObject
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzDeploymentOperation** innehåller alla åtgärder som ingick i en distribution för att hjälpa dig att identifiera och ge mer information om exakta åtgärder som misslyckades för en viss distribution.
Det kan också visa svaret och begärans innehåll för varje distribution.
Det här är samma information som i distributionsinformationen på portalen.

Om du vill hämta begäran och svarsinnehållet aktiverar du inställningen när du skickar en **distribution via New-AzDeployment.**
Det kan potentiellt logga och visa hemligheter som lösenord som används i resursegenskapen eller **listKeys-åtgärderna** som sedan returneras när du hämtar distributionsåtgärderna.
Mer information om den här inställningen och hur du aktiverar den finns i New-AzDeployment och felsöka ARM distribution av mallar

## EXEMPEL

### Exempel 1: Hämta distributionsåtgärder givet ett distributionsnamn
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

Hämtar distributionsåtgärden med "test" för namnet i den aktuella prenumerationen.

### Exempel 2: Hämta en distribution och få dess distributionsåtgärder
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

Det här kommandot får "test" för distributionen vid den aktuella prenumerationen och får distributionsåtgärder.

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

### -DeploymentName
Distributionsnamnet.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentObject
Distributionsobjektet.

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OperationId
Distributionsåtgärds-ID.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
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

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDutbetalning

## UTDATA

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDepdistributionOperation

## ANTECKNINGAR

## RELATERADE LÄNKAR
