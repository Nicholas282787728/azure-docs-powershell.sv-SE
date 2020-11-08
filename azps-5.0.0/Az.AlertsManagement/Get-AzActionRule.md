---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: 59ce466233e4997f54ed8f29835e7e64d455fb86
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270173"
---
# <span data-ttu-id="d6619-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="d6619-101">Get-AzActionRule</span></span>

## <span data-ttu-id="d6619-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6619-102">SYNOPSIS</span></span>
<span data-ttu-id="d6619-103">Information om åtgärds regler</span><span class="sxs-lookup"><span data-stu-id="d6619-103">Get Action Rules Information</span></span>

## <span data-ttu-id="d6619-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6619-104">SYNTAX</span></span>

### <span data-ttu-id="d6619-105">ListActionRules (standard)</span><span class="sxs-lookup"><span data-stu-id="d6619-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6619-106">ID</span><span class="sxs-lookup"><span data-stu-id="d6619-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6619-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="d6619-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6619-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d6619-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6619-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6619-109">DESCRIPTION</span></span>
<span data-ttu-id="d6619-110">**Get-AzActionRule** cmdlet får åtgärds regler konfigurerade.</span><span class="sxs-lookup"><span data-stu-id="d6619-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="d6619-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6619-111">EXAMPLES</span></span>

### <span data-ttu-id="d6619-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d6619-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="d6619-113">Lista alla åtgärds regler som har kon figurer ATS i resurs grupp test – RG filtrerat på Sev2 allvarlighets grad och Platform Monitor Service.</span><span class="sxs-lookup"><span data-stu-id="d6619-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="d6619-114">Använd Format-List för att få information om varje åtgärds regel i listan.</span><span class="sxs-lookup"><span data-stu-id="d6619-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="d6619-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d6619-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="d6619-116">Hämta åtgärds regeln med namn test – åtgärd-regel i test-RG resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d6619-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="d6619-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6619-117">PARAMETERS</span></span>

### <span data-ttu-id="d6619-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="d6619-118">-ActionGroup</span></span>
<span data-ttu-id="d6619-119">Åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="d6619-119">Action group</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6619-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="d6619-120">-AlertRuleId</span></span>
<span data-ttu-id="d6619-121">Filter för ID för notifieringsregel</span><span class="sxs-lookup"><span data-stu-id="d6619-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6619-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6619-122">-DefaultProfile</span></span>
<span data-ttu-id="d6619-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6619-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6619-124">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d6619-124">-Description</span></span>
<span data-ttu-id="d6619-125">Filtrera alla meddelanden med det smarta grupp-ID: t</span><span class="sxs-lookup"><span data-stu-id="d6619-125">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6619-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="d6619-126">-ImpactedScope</span></span>
<span data-ttu-id="d6619-127">Filtrera efter omfattning med påverkan</span><span class="sxs-lookup"><span data-stu-id="d6619-127">Filter on Impacted scope</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6619-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="d6619-128">-MonitorService</span></span>
<span data-ttu-id="d6619-129">Filtrera på moniter-tjänsten</span><span class="sxs-lookup"><span data-stu-id="d6619-129">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6619-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6619-130">-Name</span></span>
<span data-ttu-id="d6619-131">Namn på åtgärds regel.</span><span class="sxs-lookup"><span data-stu-id="d6619-131">Name of action rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6619-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6619-132">-ResourceGroupName</span></span>
<span data-ttu-id="d6619-133">Resurs grupp namn i vilken åtgärds regel finns.</span><span class="sxs-lookup"><span data-stu-id="d6619-133">Resource Group Name in which action rule resides.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6619-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6619-134">-ResourceId</span></span>
<span data-ttu-id="d6619-135">Hämta åtgärds regel efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d6619-135">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6619-136">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="d6619-136">-Severity</span></span>
<span data-ttu-id="d6619-137">Filtrera på allvarlighets graden för aviseringar</span><span class="sxs-lookup"><span data-stu-id="d6619-137">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6619-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d6619-138">-TargetResourceGroup</span></span>
<span data-ttu-id="d6619-139">Filtrera efter resurs grupp namn för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="d6619-139">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6619-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d6619-140">-TargetResourceId</span></span>
<span data-ttu-id="d6619-141">Filtrera efter resurs-ID för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="d6619-141">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6619-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="d6619-142">-TargetResourceType</span></span>
<span data-ttu-id="d6619-143">Filtrera efter resurs typen för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="d6619-143">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6619-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6619-144">CommonParameters</span></span>
<span data-ttu-id="d6619-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6619-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6619-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6619-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6619-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6619-147">INPUTS</span></span>

### <span data-ttu-id="d6619-148">Ingen</span><span class="sxs-lookup"><span data-stu-id="d6619-148">None</span></span>

## <span data-ttu-id="d6619-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6619-149">OUTPUTS</span></span>

### <span data-ttu-id="d6619-150">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="d6619-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="d6619-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6619-151">NOTES</span></span>

## <span data-ttu-id="d6619-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6619-152">RELATED LINKS</span></span>
