---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: a89b4210fcd498aca3a25451e6f691df20d5510e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262460"
---
# <span data-ttu-id="e0952-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="e0952-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="e0952-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0952-102">SYNOPSIS</span></span>
<span data-ttu-id="e0952-103">Hämtar information om hur du gör en lagring.</span><span class="sxs-lookup"><span data-stu-id="e0952-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="e0952-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0952-104">SYNTAX</span></span>

### <span data-ttu-id="e0952-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="e0952-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0952-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e0952-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0952-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0952-107">DESCRIPTION</span></span>
<span data-ttu-id="e0952-108">Cmdleten **Get-AzOperationalInsightsStorageInsight** hämtar information om en befintlig insyn i lagringen.</span><span class="sxs-lookup"><span data-stu-id="e0952-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="e0952-109">Om ett namn för en lagrings plats visas får denna cmdlet information om hur insynen i lagret blir.</span><span class="sxs-lookup"><span data-stu-id="e0952-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="e0952-110">Om du inte anger ett namn hämtas den här cmdleten information om alla lagrings insikter på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="e0952-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="e0952-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0952-111">EXAMPLES</span></span>

### <span data-ttu-id="e0952-112">Exempel 1: få en bättre lagring efter namn</span><span class="sxs-lookup"><span data-stu-id="e0952-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="e0952-113">Det här kommandot får dina lagrings inblickar med namnet MyStorageInsight från arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e0952-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e0952-114">Exempel 2: få en bättre lagring genom att använda ett objekt i arbets ytan</span><span class="sxs-lookup"><span data-stu-id="e0952-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="e0952-115">I det första kommandot används cmdleten **Get-AzOperationalInsightsWorkspace** för att få en arbets yta med operativa insikter och sedan lagras den i $Workspace variabel.</span><span class="sxs-lookup"><span data-stu-id="e0952-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="e0952-116">Det andra kommandot får en inblick med namnet MyStorageInsight för arbets ytan i $Workspace.</span><span class="sxs-lookup"><span data-stu-id="e0952-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="e0952-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0952-117">PARAMETERS</span></span>

### <span data-ttu-id="e0952-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0952-118">-DefaultProfile</span></span>
<span data-ttu-id="e0952-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e0952-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0952-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0952-120">-Name</span></span>
<span data-ttu-id="e0952-121">Anger namnet på lagrets inblick.</span><span class="sxs-lookup"><span data-stu-id="e0952-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0952-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0952-122">-ResourceGroupName</span></span>
<span data-ttu-id="e0952-123">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="e0952-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="e0952-124">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="e0952-124">-Workspace</span></span>
<span data-ttu-id="e0952-125">Anger arbets ytan som innehåller lagrings information.</span><span class="sxs-lookup"><span data-stu-id="e0952-125">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="e0952-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e0952-126">-WorkspaceName</span></span>
<span data-ttu-id="e0952-127">Anger namnet på den arbets yta som innehåller lagrings information.</span><span class="sxs-lookup"><span data-stu-id="e0952-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="e0952-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0952-128">CommonParameters</span></span>
<span data-ttu-id="e0952-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0952-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0952-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0952-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0952-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0952-131">INPUTS</span></span>

### <span data-ttu-id="e0952-132">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e0952-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e0952-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e0952-133">System.String</span></span>

## <span data-ttu-id="e0952-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0952-134">OUTPUTS</span></span>

### <span data-ttu-id="e0952-135">Microsoft. Azure. commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="e0952-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="e0952-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0952-136">NOTES</span></span>

## <span data-ttu-id="e0952-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0952-137">RELATED LINKS</span></span>

[<span data-ttu-id="e0952-138">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="e0952-138">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


