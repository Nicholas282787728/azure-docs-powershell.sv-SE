---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: 9c670973c9fcff3cd9038809cb955efc32edeee0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919329"
---
# <span data-ttu-id="78184-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="78184-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="78184-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78184-102">SYNOPSIS</span></span>
<span data-ttu-id="78184-103">Hämtar hanterade program</span><span class="sxs-lookup"><span data-stu-id="78184-103">Gets managed applications</span></span>

## <span data-ttu-id="78184-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78184-104">SYNTAX</span></span>

### <span data-ttu-id="78184-105">GetBySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="78184-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78184-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="78184-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78184-107">GetById</span><span class="sxs-lookup"><span data-stu-id="78184-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78184-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78184-108">DESCRIPTION</span></span>
<span data-ttu-id="78184-109">Cmdleten **Get-AzManagedApplication** hämtar hanterade program</span><span class="sxs-lookup"><span data-stu-id="78184-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="78184-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78184-110">EXAMPLES</span></span>

### <span data-ttu-id="78184-111">Exempel 1: Hämta alla hanterade program under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="78184-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="78184-112">Det här kommandot hämtar hanterade program under resurs gruppen "MyRG"</span><span class="sxs-lookup"><span data-stu-id="78184-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="78184-113">Exempel 2: Hämta alla hanterade program</span><span class="sxs-lookup"><span data-stu-id="78184-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="78184-114">Det här kommandot Hämta alla hanterade program under den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="78184-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="78184-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78184-115">PARAMETERS</span></span>

### <span data-ttu-id="78184-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="78184-116">-ApiVersion</span></span>
<span data-ttu-id="78184-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="78184-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="78184-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="78184-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="78184-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78184-119">-DefaultProfile</span></span>
<span data-ttu-id="78184-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78184-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78184-121">-ID</span><span class="sxs-lookup"><span data-stu-id="78184-121">-Id</span></span>
<span data-ttu-id="78184-122">Fullständigt kvalificerat program-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="78184-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="78184-123">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="78184-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="78184-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="78184-124">-Name</span></span>
<span data-ttu-id="78184-125">Namnet på det hanterade programmet.</span><span class="sxs-lookup"><span data-stu-id="78184-125">The managed application name.</span></span>

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

### <span data-ttu-id="78184-126">-För</span><span class="sxs-lookup"><span data-stu-id="78184-126">-Pre</span></span>
<span data-ttu-id="78184-127">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="78184-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="78184-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78184-128">-ResourceGroupName</span></span>
<span data-ttu-id="78184-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="78184-129">The resource group name.</span></span>

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

### <span data-ttu-id="78184-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78184-130">CommonParameters</span></span>
<span data-ttu-id="78184-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78184-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78184-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78184-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78184-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78184-133">INPUTS</span></span>

### <span data-ttu-id="78184-134">System. String</span><span class="sxs-lookup"><span data-stu-id="78184-134">System.String</span></span>

## <span data-ttu-id="78184-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78184-135">OUTPUTS</span></span>

### <span data-ttu-id="78184-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="78184-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="78184-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78184-137">NOTES</span></span>

## <span data-ttu-id="78184-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78184-138">RELATED LINKS</span></span>
