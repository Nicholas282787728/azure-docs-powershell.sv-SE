---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 315a44b986317157a0ada22955c04ea01726327a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525579"
---
# <span data-ttu-id="31ace-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="31ace-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="31ace-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31ace-102">SYNOPSIS</span></span>
<span data-ttu-id="31ace-103">Skapa en data koppling.</span><span class="sxs-lookup"><span data-stu-id="31ace-103">Create a Data Connector.</span></span>

## <span data-ttu-id="31ace-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31ace-104">SYNTAX</span></span>

### <span data-ttu-id="31ace-105">AzureActiveDirectory (standard)</span><span class="sxs-lookup"><span data-stu-id="31ace-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31ace-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="31ace-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31ace-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="31ace-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31ace-108">AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="31ace-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31ace-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="31ace-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31ace-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="31ace-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31ace-111">Office365</span><span class="sxs-lookup"><span data-stu-id="31ace-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31ace-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="31ace-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31ace-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31ace-113">DESCRIPTION</span></span>
<span data-ttu-id="31ace-114">Cmdleten **New-AzSentinelAlertRule** skapar en analys (notifieringsregel) på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="31ace-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="31ace-115">Du måste ange en av parametrarna, till exempel AzureActiveDirectory, för att ange vilken typ av notifieringsregel som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="31ace-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="31ace-116">Varje slag har olika obligatoriska paramaters.</span><span class="sxs-lookup"><span data-stu-id="31ace-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="31ace-117">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="31ace-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="31ace-118">Obs! alla data anslutningar i portalen är inte avaialble via API.</span><span class="sxs-lookup"><span data-stu-id="31ace-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="31ace-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31ace-119">EXAMPLES</span></span>

### <span data-ttu-id="31ace-120">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="31ace-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="31ace-121">I det här exemplet skapas en **DataConnector** för Azure Security Center på den angivna arbets ytan och sparas sedan i $DataConnector variabel.</span><span class="sxs-lookup"><span data-stu-id="31ace-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="31ace-122">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="31ace-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="31ace-123">I det här exemplet skapas en **DataConnector** för Microsoft Cloud App Security på den angivna arbets ytan och den lagrar den i $DataConnector variabel.</span><span class="sxs-lookup"><span data-stu-id="31ace-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="31ace-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31ace-124">PARAMETERS</span></span>

### <span data-ttu-id="31ace-125">-Aviseringar</span><span class="sxs-lookup"><span data-stu-id="31ace-125">-Alerts</span></span>
<span data-ttu-id="31ace-126">Data kopplings aviseringar</span><span class="sxs-lookup"><span data-stu-id="31ace-126">Data Connector Alerts</span></span>

```yaml
Type: System.String
Parameter Sets: AzureActiveDirectory, AzureAdvancedThreatProtection, AzureSecurityCenter, MicrosoftCloudAppSecurity, MicrosoftDefenderAdvancedThreatProtection
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-127">-AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="31ace-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="31ace-128">Data anslutning Amazon webb tjänst moln spårning</span><span class="sxs-lookup"><span data-stu-id="31ace-128">Data Connector Amazon Web Services Cloud Trail</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="31ace-129">-AwsRoleArn</span></span>
<span data-ttu-id="31ace-130">AWS roll ARN för data koppling</span><span class="sxs-lookup"><span data-stu-id="31ace-130">Data Connector AWS Role Arn</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-131">-AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="31ace-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="31ace-132">Data anslutning Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="31ace-132">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureActiveDirectory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="31ace-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="31ace-134">Data anslutning Avancerat skydd för Azure</span><span class="sxs-lookup"><span data-stu-id="31ace-134">Data Connector Azure Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-135">-AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="31ace-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="31ace-136">Data anslutning Azure säkerhets Center</span><span class="sxs-lookup"><span data-stu-id="31ace-136">Data Connector Azure Security Center</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="31ace-137">-DataConnectorId</span></span>
<span data-ttu-id="31ace-138">Data anslutning Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="31ace-138">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="31ace-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ace-139">-DefaultProfile</span></span>
<span data-ttu-id="31ace-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31ace-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31ace-141">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="31ace-141">-DiscoveryLogs</span></span>
<span data-ttu-id="31ace-142">Data anslutnings identifierings loggar</span><span class="sxs-lookup"><span data-stu-id="31ace-142">Data Connector Discovery Logs</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-143">-Exchange</span><span class="sxs-lookup"><span data-stu-id="31ace-143">-Exchange</span></span>
<span data-ttu-id="31ace-144">Data anslutnings utbyte</span><span class="sxs-lookup"><span data-stu-id="31ace-144">Data Connector Exchange</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-145">-Indikatorer</span><span class="sxs-lookup"><span data-stu-id="31ace-145">-Indicators</span></span>
<span data-ttu-id="31ace-146">Data kopplings indikatorer</span><span class="sxs-lookup"><span data-stu-id="31ace-146">Data Connector Indicators</span></span>

```yaml
Type: System.String
Parameter Sets: ThreatIntelligence
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-147">-Loggar</span><span class="sxs-lookup"><span data-stu-id="31ace-147">-Logs</span></span>
<span data-ttu-id="31ace-148">Data anslutnings loggar</span><span class="sxs-lookup"><span data-stu-id="31ace-148">Data Connector Logs</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="31ace-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="31ace-150">Data koppling Microsoft Cloud App-säkerhet</span><span class="sxs-lookup"><span data-stu-id="31ace-150">Data Connector Microsoft Cloud App Security</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="31ace-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="31ace-152">Data koppling Microsoft Defender Avancerat skydd</span><span class="sxs-lookup"><span data-stu-id="31ace-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftDefenderAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-153">-Office365</span><span class="sxs-lookup"><span data-stu-id="31ace-153">-Office365</span></span>
<span data-ttu-id="31ace-154">Data anslutning Office 365</span><span class="sxs-lookup"><span data-stu-id="31ace-154">Data Connector Office 365</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Office365
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ace-155">-ResourceGroupName</span></span>
<span data-ttu-id="31ace-156">Data anslutning Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="31ace-156">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="31ace-157">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="31ace-157">-SharePoint</span></span>
<span data-ttu-id="31ace-158">Data anslutning till SharePoint</span><span class="sxs-lookup"><span data-stu-id="31ace-158">Data Connector SharePoint</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31ace-159">-SubscriptionId</span></span>
<span data-ttu-id="31ace-160">Prenumerations-ID för data anslutning</span><span class="sxs-lookup"><span data-stu-id="31ace-160">Data connector Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="31ace-161">-ThreatIntelligence</span></span>
<span data-ttu-id="31ace-162">Information om data kopplingens hot</span><span class="sxs-lookup"><span data-stu-id="31ace-162">Data Connector Threat Intelligence</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ThreatIntelligence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ace-163">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="31ace-163">-WorkspaceName</span></span>
<span data-ttu-id="31ace-164">Data anslutning Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="31ace-164">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="31ace-165">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="31ace-165">-Confirm</span></span>
<span data-ttu-id="31ace-166">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="31ace-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31ace-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31ace-167">-WhatIf</span></span>
<span data-ttu-id="31ace-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="31ace-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31ace-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="31ace-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31ace-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ace-170">CommonParameters</span></span>
<span data-ttu-id="31ace-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ace-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ace-172">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31ace-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ace-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31ace-173">INPUTS</span></span>

### <span data-ttu-id="31ace-174">Ingen</span><span class="sxs-lookup"><span data-stu-id="31ace-174">None</span></span>
## <span data-ttu-id="31ace-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31ace-175">OUTPUTS</span></span>

### <span data-ttu-id="31ace-176">Microsoft. Azure. commands. SecurityInsights. Models. DataConnectors. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="31ace-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="31ace-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31ace-177">NOTES</span></span>

## <span data-ttu-id="31ace-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31ace-178">RELATED LINKS</span></span>
