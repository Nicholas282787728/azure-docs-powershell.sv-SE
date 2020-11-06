---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 5de334e5e9ac5c954770508a941a0c6fb951940d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585984"
---
# <span data-ttu-id="f3707-101">Remove-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="f3707-101">Remove-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="f3707-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3707-102">SYNOPSIS</span></span>
<span data-ttu-id="f3707-103">Tar bort en insikt om lagring.</span><span class="sxs-lookup"><span data-stu-id="f3707-103">Removes a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3707-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3707-104">SYNTAX</span></span>

### <span data-ttu-id="f3707-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="f3707-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3707-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f3707-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3707-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3707-107">DESCRIPTION</span></span>
<span data-ttu-id="f3707-108">Cmdleten **Remove-AzureRmOperationalInsightsStorageInsight** tar bort en inblick från en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="f3707-108">The **Remove-AzureRmOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="f3707-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3707-109">EXAMPLES</span></span>

### <span data-ttu-id="f3707-110">Exempel 1: ta bort en insyn i lagringen med namn</span><span class="sxs-lookup"><span data-stu-id="f3707-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="f3707-111">Det här kommandot tar bort inblick i lagrings utrymmet med namnet MyStorageInsight från arbets ytan med namnet min i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f3707-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="f3707-112">Kommandot anger inte parametern *Force* , så du uppmanas att bekräfta innan lagrets inblickar tas bort.</span><span class="sxs-lookup"><span data-stu-id="f3707-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="f3707-113">Exempel 2: ta bort en insyn i lagringen utan att bekräfta</span><span class="sxs-lookup"><span data-stu-id="f3707-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="f3707-114">I det första kommandot används cmdleten Get-AzureRmOperationalInsightsWorkspace för att hämta arbets ytan med namnet min arbets yta och den lagras sedan i $Workspace variabel. Det andra kommandot tar bort inblick i lagrings utrymmet med MyStorageInsight från $Workspace utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="f3707-114">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="f3707-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3707-115">PARAMETERS</span></span>

### <span data-ttu-id="f3707-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3707-116">-DefaultProfile</span></span>
<span data-ttu-id="f3707-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f3707-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3707-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f3707-118">-Force</span></span>
<span data-ttu-id="f3707-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f3707-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3707-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f3707-120">-Name</span></span>
<span data-ttu-id="f3707-121">Anger namnet på den inblickade lagringen.</span><span class="sxs-lookup"><span data-stu-id="f3707-121">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3707-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3707-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3707-123">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="f3707-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3707-124">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="f3707-124">-Workspace</span></span>
<span data-ttu-id="f3707-125">Anger arbets ytan som innehåller lagrings inblicken.</span><span class="sxs-lookup"><span data-stu-id="f3707-125">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3707-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f3707-126">-WorkspaceName</span></span>
<span data-ttu-id="f3707-127">Anger namnet på den arbets yta som innehåller lagrings inblicken.</span><span class="sxs-lookup"><span data-stu-id="f3707-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3707-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f3707-128">-Confirm</span></span>
<span data-ttu-id="f3707-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3707-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3707-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3707-130">-WhatIf</span></span>
<span data-ttu-id="f3707-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f3707-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3707-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f3707-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3707-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3707-133">CommonParameters</span></span>
<span data-ttu-id="f3707-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3707-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3707-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3707-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3707-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3707-136">INPUTS</span></span>

### <span data-ttu-id="f3707-137">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f3707-137">PSWorkspace</span></span>
<span data-ttu-id="f3707-138">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f3707-138">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="f3707-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3707-139">OUTPUTS</span></span>

## <span data-ttu-id="f3707-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3707-140">NOTES</span></span>

## <span data-ttu-id="f3707-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3707-141">RELATED LINKS</span></span>

[<span data-ttu-id="f3707-142">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="f3707-142">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="f3707-143">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f3707-143">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


