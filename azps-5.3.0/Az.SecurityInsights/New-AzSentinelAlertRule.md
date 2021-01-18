---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 97a07b515cff6cfd8521033dbe7380eb2a7bc1d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525586"
---
# New-AzSentinelAlertRule

## Sammanfattning
Skapa en analys (varnings regel).

## FRÅGESYNTAXEN

### ScheduledAlertRule (standard)
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FusionAlertRule
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### MicrosoftSecurityIncidentCreationRule
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzSentinelAlertRule** skapar en analys (notifieringsregel) på den angivna arbets ytan.
Du måste ange en av de tre parametrarna, *fusion*, *schemalagd* eller *MicrosoftSecurityIncidentCreation*, för att ange vilken typ av notifieringsregel som ska skapas.  Varje slag har olika obligatoriska paramaters.
Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.

## BESKRIVS

### Exempel 1
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

I det här exemplet skapas en **AlertRule** av *fusion* -typen baserat på mallen för *Avancerad skadlig* och lagrar den sedan i $AlertRule variabel.

### Exempel 2
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

I det här exemplet skapas en **AlertRule** av *MicrosoftSecurityIncidentCreation* -typen baserat på mallen för att *skapa händelser baserat på dina IoT-larm i Azure Security Center* och sedan lagras de i $AlertRule varaible.

### Exempel 2
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

I det här exemplet skapas en **DataConnector** av den *schemalagda* typen och lagrar den sedan i $AlertRule varaible.

## MALLPARAMETRAR

### -AlertRuleId
ID för notifieringsregel.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AlertRuleTemplateName
Mall för notifieringsregel.

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Beskrivning
Problembeskrivning.

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Visnings namn för aviserings regeln.

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayNamesExcludeFilter
Visnings namn för aviserings regler exkludera filter.

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayNamesFilter
Filtret visnings namn för aviserings regler.

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aktiverad
Notifieringsregel är aktive rad.

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

### -Fusion
Typ av varnings regel.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MicrosoftSecurityIncidentCreation
Typ av varnings regel.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProductFilter
Produkt filter för notifieringsregel.

```yaml
Type: System.String
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fråga
Varnings regel fråga.

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QueryFrequency
Frekvens för aviserings regel frågor.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QueryPeriod
Fråge period för aviserings regeln.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs grupps namn.

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

### -Schemalagd
Typ av varnings regel.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SeveritiesFilter
Filtret allvarlighets grader för aviseringar.

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Allvarlighets grad
Allvarlighets grad för incidenter.

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SuppressionDuration
Undertrycks tids längd för varnings regeln.

```yaml
Type: System.TimeSpan
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SuppressionEnabled
Undervisning av varnings regel aktive rad.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Taktiker
Varnings regel taktiker.

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TriggerOperator
Operator för larm regel utlösare.

```yaml
Type: Microsoft.Azure.Management.SecurityInsights.Models.TriggerOperator
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: Equal, GreaterThan, LessThan, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TriggerThreshold
Tröskel för larm regel utlösare.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Namn på arbets ytan.

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
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Ingen
## VÄRDEN

### Microsoft. Azure. commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule
## ANMÄRKNINGAR

## RELATERADE LÄNKAR
