---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: e0577342a839424d9a45a91b6c9289a72fe9df12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389016"
---
# <span data-ttu-id="461f8-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="461f8-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="461f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="461f8-102">SYNOPSIS</span></span>
<span data-ttu-id="461f8-103">Hämtar hanterade program</span><span class="sxs-lookup"><span data-stu-id="461f8-103">Gets managed applications</span></span>

## <span data-ttu-id="461f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="461f8-104">SYNTAX</span></span>

### <span data-ttu-id="461f8-105">GetBySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="461f8-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="461f8-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="461f8-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="461f8-107">GetById</span><span class="sxs-lookup"><span data-stu-id="461f8-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="461f8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="461f8-108">DESCRIPTION</span></span>
<span data-ttu-id="461f8-109">Cmdleten **Get-AzManagedApplication** hämtar hanterade program</span><span class="sxs-lookup"><span data-stu-id="461f8-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="461f8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="461f8-110">EXAMPLES</span></span>

### <span data-ttu-id="461f8-111">Exempel 1: Hämta alla hanterade program under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="461f8-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="461f8-112">Det här kommandot hämtar hanterade program under resurs gruppen "MyRG"</span><span class="sxs-lookup"><span data-stu-id="461f8-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="461f8-113">Exempel 2: Hämta alla hanterade program</span><span class="sxs-lookup"><span data-stu-id="461f8-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="461f8-114">Det här kommandot Hämta alla hanterade program under den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="461f8-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="461f8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="461f8-115">PARAMETERS</span></span>

### <span data-ttu-id="461f8-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="461f8-116">-ApiVersion</span></span>
<span data-ttu-id="461f8-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="461f8-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="461f8-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="461f8-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="461f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="461f8-119">-DefaultProfile</span></span>
<span data-ttu-id="461f8-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="461f8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="461f8-121">-ID</span><span class="sxs-lookup"><span data-stu-id="461f8-121">-Id</span></span>
<span data-ttu-id="461f8-122">Fullständigt kvalificerat program-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="461f8-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="461f8-123">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="461f8-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="461f8-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="461f8-124">-Name</span></span>
<span data-ttu-id="461f8-125">Namnet på det hanterade programmet.</span><span class="sxs-lookup"><span data-stu-id="461f8-125">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="461f8-126">-För</span><span class="sxs-lookup"><span data-stu-id="461f8-126">-Pre</span></span>
<span data-ttu-id="461f8-127">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="461f8-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="461f8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="461f8-128">-ResourceGroupName</span></span>
<span data-ttu-id="461f8-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="461f8-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="461f8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="461f8-130">CommonParameters</span></span>
<span data-ttu-id="461f8-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="461f8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="461f8-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="461f8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="461f8-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="461f8-133">INPUTS</span></span>

### <span data-ttu-id="461f8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="461f8-134">System.String</span></span>

## <span data-ttu-id="461f8-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="461f8-135">OUTPUTS</span></span>

### <span data-ttu-id="461f8-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="461f8-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="461f8-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="461f8-137">NOTES</span></span>

## <span data-ttu-id="461f8-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="461f8-138">RELATED LINKS</span></span>
