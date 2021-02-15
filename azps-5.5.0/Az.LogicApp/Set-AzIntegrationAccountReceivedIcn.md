---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 146f1ba93a8df5f6a4396c30c9da451cdb89b9b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221622"
---
# Set-AzIntegrationAccountReceivedIcn

## SYNOPSIS
Uppdaterar integrationskontot mottaget överföringskontrollnummer (ICN) i Azure-resursgruppen.

## SYNTAX

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten Set-AzIntegrationAccountGeneratedIcn uppdaterar ett befintligt integrationskonto mottaget överföringskontrollnummer (ICN) och returnerar ett objekt som representerar det integrationskonto som mottagit överföringskontrollnummer.
Använd denna cmdlet för att uppdatera statusen för ett mottaget integrationskonto för överföringskontrollnumrets meddelandebearbetningsstatus.
Du kan uppdatera ett mottaget överföringskontrollnummer för ett integrationskonto genom att ange namnet på integrationskontot, namnet på resursgruppen, avtalsnamnet, kontrollnumret och meddelandebearbetningsstatusen.
Du kan inte skapa ett nytt integrationskonto som du fått överföringskontrollnumret för med det här kommandot.
Om du vill använda de dynamiska parametrarna skriver du dem i kommandot eller skriver ett bindestreck(-) för att ange ett parameternamn och trycker sedan på TABB-tangenten flera gånger för att växla mellan tillgängliga parametrar.
Om du missar en obligatorisk mallparameter uppmanas du att ange värdet i cmdleten.
Mallparameterfilvärden som du anger på kommandoraden har företräde framför mallparametervärden i ett mallparameterobjekt.
Ange parametern "-AgreementType" för att ange om X12- eller Edifact-kontrollnummer ska returneras

## EXEMPEL

### Exempel 1
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

Det här kommandot uppdaterar det integrationskonto som fått X12 överföringskontrollnumret för ett visst avtal för integrationskontot och värdet med statusen för meddelandebearbetning misslyckades.

### Exempel 2
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

Det här kommandot uppdaterar det integrationskonto som mottagits Edifact interchange control number för ett visst avtal för integrationskonto och värde med statusen för meddelandebearbetning misslyckades.

## PARAMETERS

### -AgreementName
Namnet på avtalet för integrationskonto.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AgreementType
Avtalstyp för integrationskonto (X12 eller Edifact).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ControlNumberValue
Värdet för integrationskontots kontrollnummer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -IsMessageProcessingFailed
Status för det mottagna meddelandets bearbetningsstatus.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Namnet på integrationskontot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resursen för integrationskontot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System.String

## UTDATA

### Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)
