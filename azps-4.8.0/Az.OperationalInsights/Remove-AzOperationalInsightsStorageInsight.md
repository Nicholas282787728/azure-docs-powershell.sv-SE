---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: ac9e061fea8c6d7737eb268feec225dff0b0924d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258097"
---
# <span data-ttu-id="1865c-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="1865c-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="1865c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1865c-102">SYNOPSIS</span></span>
<span data-ttu-id="1865c-103">Tar bort en insikt om lagring.</span><span class="sxs-lookup"><span data-stu-id="1865c-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="1865c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1865c-104">SYNTAX</span></span>

### <span data-ttu-id="1865c-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="1865c-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1865c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1865c-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1865c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1865c-107">DESCRIPTION</span></span>
<span data-ttu-id="1865c-108">Cmdleten **Remove-AzOperationalInsightsStorageInsight** tar bort en inblick från en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="1865c-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="1865c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1865c-109">EXAMPLES</span></span>

### <span data-ttu-id="1865c-110">Exempel 1: ta bort en insyn i lagringen med namn</span><span class="sxs-lookup"><span data-stu-id="1865c-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="1865c-111">Det här kommandot tar bort inblick i lagrings utrymmet med namnet MyStorageInsight från arbets ytan med namnet min i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1865c-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="1865c-112">Kommandot anger inte parametern *Force* , så du uppmanas att bekräfta innan lagrets inblickar tas bort.</span><span class="sxs-lookup"><span data-stu-id="1865c-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="1865c-113">Exempel 2: ta bort en insyn i lagringen utan att bekräfta</span><span class="sxs-lookup"><span data-stu-id="1865c-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="1865c-114">I det första kommandot används cmdleten Get-AzOperationalInsightsWorkspace för att hämta arbets ytan med namnet min arbets yta och den lagras sedan i $Workspace variabel. Det andra kommandot tar bort inblick i lagrings utrymmet med MyStorageInsight från $Workspace utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1865c-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="1865c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1865c-115">PARAMETERS</span></span>

### <span data-ttu-id="1865c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1865c-116">-DefaultProfile</span></span>
<span data-ttu-id="1865c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1865c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1865c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1865c-118">-Force</span></span>
<span data-ttu-id="1865c-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1865c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1865c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="1865c-120">-Name</span></span>
<span data-ttu-id="1865c-121">Anger namnet på den inblickade lagringen.</span><span class="sxs-lookup"><span data-stu-id="1865c-121">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1865c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1865c-122">-ResourceGroupName</span></span>
<span data-ttu-id="1865c-123">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="1865c-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1865c-124">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="1865c-124">-Workspace</span></span>
<span data-ttu-id="1865c-125">Anger arbets ytan som innehåller lagrings inblicken.</span><span class="sxs-lookup"><span data-stu-id="1865c-125">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1865c-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1865c-126">-WorkspaceName</span></span>
<span data-ttu-id="1865c-127">Anger namnet på den arbets yta som innehåller lagrings inblicken.</span><span class="sxs-lookup"><span data-stu-id="1865c-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1865c-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1865c-128">-Confirm</span></span>
<span data-ttu-id="1865c-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1865c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1865c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1865c-130">-WhatIf</span></span>
<span data-ttu-id="1865c-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1865c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1865c-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1865c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1865c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1865c-133">CommonParameters</span></span>
<span data-ttu-id="1865c-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1865c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1865c-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1865c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1865c-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1865c-136">INPUTS</span></span>

### <span data-ttu-id="1865c-137">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1865c-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="1865c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1865c-138">System.String</span></span>

## <span data-ttu-id="1865c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1865c-139">OUTPUTS</span></span>

### <span data-ttu-id="1865c-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="1865c-140">System.Void</span></span>

## <span data-ttu-id="1865c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1865c-141">NOTES</span></span>

## <span data-ttu-id="1865c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1865c-142">RELATED LINKS</span></span>

[<span data-ttu-id="1865c-143">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="1865c-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="1865c-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1865c-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


