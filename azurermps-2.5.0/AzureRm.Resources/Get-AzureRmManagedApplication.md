---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplication
schema: 2.0.0
ms.openlocfilehash: 482bf9a2158fc299d78c993255e390dc480245a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930110"
---
# <span data-ttu-id="fec3f-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="fec3f-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="fec3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fec3f-102">SYNOPSIS</span></span>
<span data-ttu-id="fec3f-103">Hämtar hanterade program</span><span class="sxs-lookup"><span data-stu-id="fec3f-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fec3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fec3f-104">SYNTAX</span></span>

### <span data-ttu-id="fec3f-105">GetBySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="fec3f-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fec3f-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fec3f-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fec3f-107">GetById</span><span class="sxs-lookup"><span data-stu-id="fec3f-107">GetById</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fec3f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fec3f-108">DESCRIPTION</span></span>
<span data-ttu-id="fec3f-109">Cmdleten **Get-AzureRmManagedApplication** hämtar hanterade program</span><span class="sxs-lookup"><span data-stu-id="fec3f-109">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="fec3f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fec3f-110">EXAMPLES</span></span>

### <span data-ttu-id="fec3f-111">Exempel 1: Hämta alla hanterade program under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="fec3f-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="fec3f-112">Det här kommandot hämtar hanterade program under resurs gruppen "MyRG"</span><span class="sxs-lookup"><span data-stu-id="fec3f-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="fec3f-113">Exempel 2: Hämta alla hanterade program</span><span class="sxs-lookup"><span data-stu-id="fec3f-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="fec3f-114">Det här kommandot Hämta alla hanterade program under den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="fec3f-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="fec3f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fec3f-115">PARAMETERS</span></span>

### <span data-ttu-id="fec3f-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fec3f-116">-ApiVersion</span></span>
<span data-ttu-id="fec3f-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="fec3f-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fec3f-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="fec3f-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec3f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec3f-119">-DefaultProfile</span></span>
<span data-ttu-id="fec3f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fec3f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fec3f-121">-ID</span><span class="sxs-lookup"><span data-stu-id="fec3f-121">-Id</span></span>
<span data-ttu-id="fec3f-122">Fullständigt kvalificerat program-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="fec3f-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="fec3f-123">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="fec3f-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fec3f-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="fec3f-124">-Name</span></span>
<span data-ttu-id="fec3f-125">Namnet på det hanterade programmet.</span><span class="sxs-lookup"><span data-stu-id="fec3f-125">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fec3f-126">-För</span><span class="sxs-lookup"><span data-stu-id="fec3f-126">-Pre</span></span>
<span data-ttu-id="fec3f-127">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="fec3f-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fec3f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fec3f-128">-ResourceGroupName</span></span>
<span data-ttu-id="fec3f-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fec3f-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fec3f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec3f-130">CommonParameters</span></span>
<span data-ttu-id="fec3f-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec3f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec3f-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fec3f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec3f-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fec3f-133">INPUTS</span></span>

### <span data-ttu-id="fec3f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fec3f-134">System.String</span></span>

## <span data-ttu-id="fec3f-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fec3f-135">OUTPUTS</span></span>

### <span data-ttu-id="fec3f-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fec3f-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fec3f-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fec3f-137">NOTES</span></span>

## <span data-ttu-id="fec3f-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fec3f-138">RELATED LINKS</span></span>
