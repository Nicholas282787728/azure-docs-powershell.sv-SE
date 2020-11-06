---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: b0d3baaa1e41e6f0df74e1b6bf39bdc858777a92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572688"
---
# <span data-ttu-id="b6654-101">Get-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="b6654-101">Get-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="b6654-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6654-102">SYNOPSIS</span></span>
<span data-ttu-id="b6654-103">Hämtar information om hur du gör en lagring.</span><span class="sxs-lookup"><span data-stu-id="b6654-103">Gets information about a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6654-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6654-104">SYNTAX</span></span>

### <span data-ttu-id="b6654-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="b6654-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6654-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b6654-106">ByWorkspaceObject</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6654-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6654-107">DESCRIPTION</span></span>
<span data-ttu-id="b6654-108">Cmdleten **Get-AzureRmOperationalInsightsStorageInsight** hämtar information om en befintlig insyn i lagringen.</span><span class="sxs-lookup"><span data-stu-id="b6654-108">The **Get-AzureRmOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="b6654-109">Om ett namn för en lagrings plats visas får denna cmdlet information om hur insynen i lagret blir.</span><span class="sxs-lookup"><span data-stu-id="b6654-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="b6654-110">Om du inte anger ett namn hämtas den här cmdleten information om alla lagrings insikter på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="b6654-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="b6654-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6654-111">EXAMPLES</span></span>

### <span data-ttu-id="b6654-112">Exempel 1: få en bättre lagring efter namn</span><span class="sxs-lookup"><span data-stu-id="b6654-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="b6654-113">Det här kommandot får dina lagrings inblickar med namnet MyStorageInsight från arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b6654-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="b6654-114">Exempel 2: få en bättre lagring genom att använda ett objekt i arbets ytan</span><span class="sxs-lookup"><span data-stu-id="b6654-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="b6654-115">I det första kommandot används cmdleten **Get-AzureRmOperationalInsightsWorkspace** för att få en arbets yta med operativa insikter och sedan lagras den i $Workspace variabel.</span><span class="sxs-lookup"><span data-stu-id="b6654-115">The first command uses the **Get-AzureRmOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="b6654-116">Det andra kommandot får en inblick med namnet MyStorageInsight för arbets ytan i $Workspace.</span><span class="sxs-lookup"><span data-stu-id="b6654-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="b6654-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6654-117">PARAMETERS</span></span>

### <span data-ttu-id="b6654-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6654-118">-DefaultProfile</span></span>
<span data-ttu-id="b6654-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b6654-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6654-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b6654-120">-Name</span></span>
<span data-ttu-id="b6654-121">Anger namnet på lagrets inblick.</span><span class="sxs-lookup"><span data-stu-id="b6654-121">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="b6654-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6654-122">-ResourceGroupName</span></span>
<span data-ttu-id="b6654-123">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="b6654-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="b6654-124">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="b6654-124">-Workspace</span></span>
<span data-ttu-id="b6654-125">Anger arbets ytan som innehåller lagrings information.</span><span class="sxs-lookup"><span data-stu-id="b6654-125">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="b6654-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b6654-126">-WorkspaceName</span></span>
<span data-ttu-id="b6654-127">Anger namnet på den arbets yta som innehåller lagrings information.</span><span class="sxs-lookup"><span data-stu-id="b6654-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="b6654-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6654-128">CommonParameters</span></span>
<span data-ttu-id="b6654-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6654-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6654-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6654-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6654-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6654-131">INPUTS</span></span>

### <span data-ttu-id="b6654-132">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b6654-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="b6654-133">Parametrar: arbets yta (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b6654-133">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="b6654-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b6654-134">System.String</span></span>

## <span data-ttu-id="b6654-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6654-135">OUTPUTS</span></span>

### <span data-ttu-id="b6654-136">Microsoft. Azure. commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="b6654-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="b6654-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6654-137">NOTES</span></span>

## <span data-ttu-id="b6654-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6654-138">RELATED LINKS</span></span>

[<span data-ttu-id="b6654-139">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="b6654-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


