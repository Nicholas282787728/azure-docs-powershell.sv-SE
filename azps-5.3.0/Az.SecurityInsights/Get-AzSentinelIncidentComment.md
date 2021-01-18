---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: d33c126da2a77736871a9ec1f950382168f52bee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525587"
---
# <span data-ttu-id="5235d-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="5235d-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="5235d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5235d-102">SYNOPSIS</span></span>
<span data-ttu-id="5235d-103">Få en incident kommentar.</span><span class="sxs-lookup"><span data-stu-id="5235d-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="5235d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5235d-104">SYNTAX</span></span>

### <span data-ttu-id="5235d-105">IncidentId (standard)</span><span class="sxs-lookup"><span data-stu-id="5235d-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5235d-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="5235d-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5235d-107">ID</span><span class="sxs-lookup"><span data-stu-id="5235d-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5235d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5235d-108">DESCRIPTION</span></span>
<span data-ttu-id="5235d-109">Cmdleten **Get-AzSentinelIncidentComment** får en incident kommentar från den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="5235d-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="5235d-110">Om du anger parametrarna *IncidentCommentId* och *IncidentId* returneras ett enskilt **IncidentComment** -objekt.</span><span class="sxs-lookup"><span data-stu-id="5235d-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="5235d-111">Om du inte anger parametern *IncidentCommentId* returneras en matris med alla incident kommentarer för den angivna incidenten på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="5235d-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="5235d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5235d-112">EXAMPLES</span></span>

### <span data-ttu-id="5235d-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5235d-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="5235d-114">I det här exemplet hämtas alla **IncidentComments** för angiven incident på den angivna arbets ytan och sparas sedan i $IncidentComments variabel.</span><span class="sxs-lookup"><span data-stu-id="5235d-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="5235d-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5235d-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="5235d-116">Det här exemplet får en **IncidentComment** för den angivna incidenten på den angivna arbets ytan och lagrar den sedan i $IncidentComment variabel.</span><span class="sxs-lookup"><span data-stu-id="5235d-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="5235d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5235d-117">PARAMETERS</span></span>

### <span data-ttu-id="5235d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5235d-118">-DefaultProfile</span></span>
<span data-ttu-id="5235d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5235d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5235d-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="5235d-120">-IncidentCommentId</span></span>
<span data-ttu-id="5235d-121">ID för incident kommentar.</span><span class="sxs-lookup"><span data-stu-id="5235d-121">Incident Comment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5235d-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="5235d-122">-IncidentId</span></span>
<span data-ttu-id="5235d-123">Incident-ID.</span><span class="sxs-lookup"><span data-stu-id="5235d-123">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5235d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5235d-124">-ResourceGroupName</span></span>
<span data-ttu-id="5235d-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5235d-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5235d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5235d-126">-ResourceId</span></span>
<span data-ttu-id="5235d-127">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5235d-127">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5235d-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5235d-128">-WorkspaceName</span></span>
<span data-ttu-id="5235d-129">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="5235d-129">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5235d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5235d-130">CommonParameters</span></span>
<span data-ttu-id="5235d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5235d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5235d-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5235d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5235d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5235d-133">INPUTS</span></span>

### <span data-ttu-id="5235d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5235d-134">System.String</span></span>
## <span data-ttu-id="5235d-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5235d-135">OUTPUTS</span></span>

### <span data-ttu-id="5235d-136">Microsoft. Azure. commands. SecurityInsights. Models. IncidentComments. PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="5235d-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="5235d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5235d-137">NOTES</span></span>

## <span data-ttu-id="5235d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5235d-138">RELATED LINKS</span></span>
