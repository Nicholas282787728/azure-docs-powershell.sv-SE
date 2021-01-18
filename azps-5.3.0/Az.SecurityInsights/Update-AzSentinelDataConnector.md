---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: b998d699836cf99f9d6cb9dc53bef36b6fc94ca3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525554"
---
# <span data-ttu-id="3cf11-101">Update-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="3cf11-101">Update-AzSentinelDataConnector</span></span>

## <span data-ttu-id="3cf11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3cf11-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf11-103">Uppdatera en data anslutning.</span><span class="sxs-lookup"><span data-stu-id="3cf11-103">Update a Data Connector.</span></span>

## <span data-ttu-id="3cf11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3cf11-104">SYNTAX</span></span>

### <span data-ttu-id="3cf11-105">DataConnectorId (standard)</span><span class="sxs-lookup"><span data-stu-id="3cf11-105">DataConnectorId (Default)</span></span>
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf11-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3cf11-106">InputObject</span></span>
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf11-107">ID</span><span class="sxs-lookup"><span data-stu-id="3cf11-107">ResourceId</span></span>
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cf11-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3cf11-108">DESCRIPTION</span></span>
<span data-ttu-id="3cf11-109">Cmdleten **Update-AzSentinelDataConnector** uppdaterar data kopplingen på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="3cf11-109">The **Update-AzSentinelDataConnector** cmdlet updates the Data Connector in the specified workspace.</span></span>
<span data-ttu-id="3cf11-110">Du kan skicka ett **DataConnector** -objekt som en parameter eller med hjälp av pipeline-operatorn eller så kan du ange de parametrar som krävs.</span><span class="sxs-lookup"><span data-stu-id="3cf11-110">You can pass an **DataConnector** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="3cf11-111">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="3cf11-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="3cf11-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3cf11-112">EXAMPLES</span></span>

### <span data-ttu-id="3cf11-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3cf11-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

<span data-ttu-id="3cf11-114">Kommandot hämtar data kopplingen genom *DataConnectorId* och anger läget för *aviseringar* till *inaktive rad*.</span><span class="sxs-lookup"><span data-stu-id="3cf11-114">The command gets the Data Connector by *DataConnectorId* and sets the *Alerts* state to *Disabled*.</span></span>  <span data-ttu-id="3cf11-115">Alla andra egenskaper förblir desamma.</span><span class="sxs-lookup"><span data-stu-id="3cf11-115">All other properties remain the same.</span></span>

## <span data-ttu-id="3cf11-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3cf11-116">PARAMETERS</span></span>

### <span data-ttu-id="3cf11-117">-Aviseringar</span><span class="sxs-lookup"><span data-stu-id="3cf11-117">-Alerts</span></span>
<span data-ttu-id="3cf11-118">Data kopplings aviseringar</span><span class="sxs-lookup"><span data-stu-id="3cf11-118">Data Connector Alerts</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-119">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="3cf11-119">-AwsRoleArn</span></span>
<span data-ttu-id="3cf11-120">AWS roll ARN för data koppling</span><span class="sxs-lookup"><span data-stu-id="3cf11-120">Data Connector AWS Role Arn</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-121">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="3cf11-121">-DataConnectorId</span></span>
<span data-ttu-id="3cf11-122">ID för data anslutning.</span><span class="sxs-lookup"><span data-stu-id="3cf11-122">Data Connector Id.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf11-123">-DefaultProfile</span></span>
<span data-ttu-id="3cf11-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf11-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-125">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="3cf11-125">-DiscoveryLogs</span></span>
<span data-ttu-id="3cf11-126">Data anslutnings identifierings loggar</span><span class="sxs-lookup"><span data-stu-id="3cf11-126">Data Connector Discovery Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-127">-Exchange</span><span class="sxs-lookup"><span data-stu-id="3cf11-127">-Exchange</span></span>
<span data-ttu-id="3cf11-128">Data anslutnings utbyte</span><span class="sxs-lookup"><span data-stu-id="3cf11-128">Data Connector Exchange</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-129">-Indikatorer</span><span class="sxs-lookup"><span data-stu-id="3cf11-129">-Indicators</span></span>
<span data-ttu-id="3cf11-130">Data kopplings indikatorer</span><span class="sxs-lookup"><span data-stu-id="3cf11-130">Data Connector Indicators</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cf11-131">-InputObject</span></span>
<span data-ttu-id="3cf11-132">InputObject.</span><span class="sxs-lookup"><span data-stu-id="3cf11-132">InputObject.</span></span>

```yaml
Type: PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-133">-Loggar</span><span class="sxs-lookup"><span data-stu-id="3cf11-133">-Logs</span></span>
<span data-ttu-id="3cf11-134">Data anslutnings loggar</span><span class="sxs-lookup"><span data-stu-id="3cf11-134">Data Connector Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf11-135">-ResourceGroupName</span></span>
<span data-ttu-id="3cf11-136">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3cf11-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cf11-137">-ResourceId</span></span>
<span data-ttu-id="3cf11-138">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3cf11-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-139">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="3cf11-139">-SharePoint</span></span>
<span data-ttu-id="3cf11-140">Data anslutning till SharePoint</span><span class="sxs-lookup"><span data-stu-id="3cf11-140">Data Connector SharePoint</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3cf11-141">-SubscriptionId</span></span>
<span data-ttu-id="3cf11-142">Prenumerations-ID för data anslutning</span><span class="sxs-lookup"><span data-stu-id="3cf11-142">Data connector Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3cf11-143">-WorkspaceName</span></span>
<span data-ttu-id="3cf11-144">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="3cf11-144">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3cf11-145">-Confirm</span></span>
<span data-ttu-id="3cf11-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3cf11-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf11-147">-WhatIf</span></span>
<span data-ttu-id="3cf11-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3cf11-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cf11-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3cf11-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf11-150">CommonParameters</span></span>
<span data-ttu-id="3cf11-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf11-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf11-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cf11-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf11-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3cf11-153">INPUTS</span></span>

### <span data-ttu-id="3cf11-154">Microsoft. Azure. commands. SecurityInsights. Models. DataConnectors. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="3cf11-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

### <span data-ttu-id="3cf11-155">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf11-155">System.String</span></span>

## <span data-ttu-id="3cf11-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3cf11-156">OUTPUTS</span></span>

### <span data-ttu-id="3cf11-157">Microsoft. Azure. commands. SecurityInsights. Models. DataConnectors. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="3cf11-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

## <span data-ttu-id="3cf11-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3cf11-158">NOTES</span></span>

## <span data-ttu-id="3cf11-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3cf11-159">RELATED LINKS</span></span>
