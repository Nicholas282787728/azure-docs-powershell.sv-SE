---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: cbbbd23a42f2922273811a7925cbae6f6fd867f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575910"
---
# <span data-ttu-id="6b1c7-101">Remove-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="6b1c7-101">Remove-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="6b1c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b1c7-102">SYNOPSIS</span></span>
<span data-ttu-id="6b1c7-103">Tar bort en insikt om lagring.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-103">Removes a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b1c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b1c7-104">SYNTAX</span></span>

### <span data-ttu-id="6b1c7-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="6b1c7-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b1c7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6b1c7-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b1c7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b1c7-107">DESCRIPTION</span></span>
<span data-ttu-id="6b1c7-108">Cmdleten **Remove-AzureRmOperationalInsightsStorageInsight** tar bort en inblick från en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-108">The **Remove-AzureRmOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="6b1c7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b1c7-109">EXAMPLES</span></span>

### <span data-ttu-id="6b1c7-110">Exempel 1: ta bort en insyn i lagringen med namn</span><span class="sxs-lookup"><span data-stu-id="6b1c7-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="6b1c7-111">Det här kommandot tar bort inblick i lagrings utrymmet med namnet MyStorageInsight från arbets ytan med namnet min i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="6b1c7-112">Kommandot anger inte parametern *Force* , så du uppmanas att bekräfta innan lagrets inblickar tas bort.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="6b1c7-113">Exempel 2: ta bort en insyn i lagringen utan att bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b1c7-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="6b1c7-114">I det första kommandot används cmdleten Get-AzureRmOperationalInsightsWorkspace för att hämta arbets ytan med namnet min arbets yta och den lagras sedan i $Workspace variabel. Det andra kommandot tar bort inblick i lagrings utrymmet med MyStorageInsight från $Workspace utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-114">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="6b1c7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b1c7-115">PARAMETERS</span></span>

### <span data-ttu-id="6b1c7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6b1c7-116">-Force</span></span>
<span data-ttu-id="6b1c7-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6b1c7-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="6b1c7-118">-Name</span></span>
<span data-ttu-id="6b1c7-119">Anger namnet på den inblickade lagringen.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-119">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="6b1c7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b1c7-120">-ResourceGroupName</span></span>
<span data-ttu-id="6b1c7-121">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-121">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="6b1c7-122">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="6b1c7-122">-Workspace</span></span>
<span data-ttu-id="6b1c7-123">Anger arbets ytan som innehåller lagrings inblicken.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-123">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="6b1c7-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6b1c7-124">-WorkspaceName</span></span>
<span data-ttu-id="6b1c7-125">Anger namnet på den arbets yta som innehåller lagrings inblicken.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-125">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="6b1c7-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b1c7-126">-Confirm</span></span>
<span data-ttu-id="6b1c7-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b1c7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b1c7-128">-WhatIf</span></span>
<span data-ttu-id="6b1c7-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b1c7-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b1c7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b1c7-131">-DefaultProfile</span></span>
<span data-ttu-id="6b1c7-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b1c7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b1c7-133">CommonParameters</span></span>
<span data-ttu-id="6b1c7-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b1c7-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b1c7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b1c7-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b1c7-136">INPUTS</span></span>

### <span data-ttu-id="6b1c7-137">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6b1c7-137">PSWorkspace</span></span>
<span data-ttu-id="6b1c7-138">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6b1c7-138">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="6b1c7-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b1c7-139">OUTPUTS</span></span>

## <span data-ttu-id="6b1c7-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b1c7-140">NOTES</span></span>

## <span data-ttu-id="6b1c7-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b1c7-141">RELATED LINKS</span></span>

[<span data-ttu-id="6b1c7-142">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="6b1c7-142">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="6b1c7-143">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="6b1c7-143">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)

