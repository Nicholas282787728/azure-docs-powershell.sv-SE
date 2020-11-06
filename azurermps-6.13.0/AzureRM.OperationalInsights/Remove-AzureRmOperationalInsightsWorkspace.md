---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 5a222b404aa931cec468ee5dfc66963f48b23ada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573957"
---
# <span data-ttu-id="97feb-101">Remove-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="97feb-101">Remove-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="97feb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97feb-102">SYNOPSIS</span></span>
<span data-ttu-id="97feb-103">Tar bort en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="97feb-103">Removes a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97feb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97feb-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97feb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97feb-105">DESCRIPTION</span></span>
<span data-ttu-id="97feb-106">Cmdleten **Remove-AzureRmOperationalInsightsWorkspace** tar bort en befintlig arbets yta.</span><span class="sxs-lookup"><span data-stu-id="97feb-106">The **Remove-AzureRmOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="97feb-107">Om den här arbets ytan har länkats till ett befintligt konto via parametern *CustomerId* när det skapades, tas inte original kontot bort i den operativa insikts portalen.</span><span class="sxs-lookup"><span data-stu-id="97feb-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="97feb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97feb-108">EXAMPLES</span></span>

### <span data-ttu-id="97feb-109">Exempel 1: ta bort en arbets yta efter namn</span><span class="sxs-lookup"><span data-stu-id="97feb-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="97feb-110">Det här kommandot tar bort arbets ytan med namnet min arbets yta från resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="97feb-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="97feb-111">Exempel 2: ta bort en arbets yta med hjälp av pipeline och utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="97feb-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

<span data-ttu-id="97feb-112">Det här kommandot använder cmdleten Get-AzureRmOperationalInsightsWorkspace för att hämta arbets ytan med namnet min arbets yta och skickar den till cmdlet **Remove-AzureRmOperationalInsightsWorkspace** genom att använda pipeline-operatorn för att ta bort den.</span><span class="sxs-lookup"><span data-stu-id="97feb-112">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="97feb-113">Eftersom parametern *Force* är angiven får du inte en uppmaning om att ta bort arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="97feb-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="97feb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97feb-114">PARAMETERS</span></span>

### <span data-ttu-id="97feb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97feb-115">-DefaultProfile</span></span>
<span data-ttu-id="97feb-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="97feb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97feb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="97feb-117">-Force</span></span>
<span data-ttu-id="97feb-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="97feb-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97feb-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="97feb-119">-Name</span></span>
<span data-ttu-id="97feb-120">Anger namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="97feb-120">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="97feb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97feb-121">-ResourceGroupName</span></span>
<span data-ttu-id="97feb-122">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="97feb-122">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="97feb-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97feb-123">-Confirm</span></span>
<span data-ttu-id="97feb-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97feb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97feb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97feb-125">-WhatIf</span></span>
<span data-ttu-id="97feb-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97feb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97feb-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97feb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97feb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97feb-128">CommonParameters</span></span>
<span data-ttu-id="97feb-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97feb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97feb-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97feb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97feb-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97feb-131">INPUTS</span></span>

### <span data-ttu-id="97feb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="97feb-132">System.String</span></span>

## <span data-ttu-id="97feb-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97feb-133">OUTPUTS</span></span>

### <span data-ttu-id="97feb-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="97feb-134">System.Void</span></span>

## <span data-ttu-id="97feb-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97feb-135">NOTES</span></span>

## <span data-ttu-id="97feb-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97feb-136">RELATED LINKS</span></span>

[<span data-ttu-id="97feb-137">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="97feb-137">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="97feb-138">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="97feb-138">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


