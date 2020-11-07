---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 9758c0dda8d392100e57909edca310f14d3746af
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755155"
---
# <span data-ttu-id="ef428-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ef428-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="ef428-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef428-102">SYNOPSIS</span></span>
<span data-ttu-id="ef428-103">Tar bort en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="ef428-103">Removes a workspace.</span></span>

## <span data-ttu-id="ef428-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef428-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef428-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef428-105">DESCRIPTION</span></span>
<span data-ttu-id="ef428-106">Cmdleten **Remove-AzOperationalInsightsWorkspace** tar bort en befintlig arbets yta.</span><span class="sxs-lookup"><span data-stu-id="ef428-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="ef428-107">Om den här arbets ytan har länkats till ett befintligt konto via parametern *CustomerId* när det skapades, tas inte original kontot bort i den operativa insikts portalen.</span><span class="sxs-lookup"><span data-stu-id="ef428-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="ef428-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef428-108">EXAMPLES</span></span>

### <span data-ttu-id="ef428-109">Exempel 1: ta bort en arbets yta efter namn</span><span class="sxs-lookup"><span data-stu-id="ef428-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="ef428-110">Det här kommandot tar bort arbets ytan med namnet min arbets yta från resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ef428-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="ef428-111">Exempel 2: ta bort en arbets yta med hjälp av pipeline och utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="ef428-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="ef428-112">Det här kommandot använder cmdleten Get-AzOperationalInsightsWorkspace för att hämta arbets ytan med namnet min arbets yta och skickar den till cmdlet **Remove-AzOperationalInsightsWorkspace** genom att använda pipeline-operatorn för att ta bort den.</span><span class="sxs-lookup"><span data-stu-id="ef428-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="ef428-113">Eftersom parametern *Force* är angiven får du inte en uppmaning om att ta bort arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="ef428-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="ef428-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef428-114">PARAMETERS</span></span>

### <span data-ttu-id="ef428-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef428-115">-DefaultProfile</span></span>
<span data-ttu-id="ef428-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ef428-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef428-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ef428-117">-Force</span></span>
<span data-ttu-id="ef428-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ef428-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ef428-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef428-119">-Name</span></span>
<span data-ttu-id="ef428-120">Anger namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="ef428-120">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef428-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef428-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef428-122">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="ef428-122">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef428-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef428-123">-Confirm</span></span>
<span data-ttu-id="ef428-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef428-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef428-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef428-125">-WhatIf</span></span>
<span data-ttu-id="ef428-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef428-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef428-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef428-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef428-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef428-128">CommonParameters</span></span>
<span data-ttu-id="ef428-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef428-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef428-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef428-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef428-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef428-131">INPUTS</span></span>

### <span data-ttu-id="ef428-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ef428-132">System.String</span></span>

## <span data-ttu-id="ef428-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef428-133">OUTPUTS</span></span>

### <span data-ttu-id="ef428-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="ef428-134">System.Void</span></span>

## <span data-ttu-id="ef428-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef428-135">NOTES</span></span>

## <span data-ttu-id="ef428-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef428-136">RELATED LINKS</span></span>

[<span data-ttu-id="ef428-137">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="ef428-137">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="ef428-138">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ef428-138">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


