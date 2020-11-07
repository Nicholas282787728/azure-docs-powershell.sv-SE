---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: e6df93dee8599c6bae42cc9428b2a7691abf4740
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930106"
---
# <span data-ttu-id="39dd7-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="39dd7-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="39dd7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="39dd7-103">Hämtar definitioner för hanterade program</span><span class="sxs-lookup"><span data-stu-id="39dd7-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39dd7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39dd7-104">SYNTAX</span></span>

### <span data-ttu-id="39dd7-105">GetByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="39dd7-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39dd7-106">GetById</span><span class="sxs-lookup"><span data-stu-id="39dd7-106">GetById</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39dd7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39dd7-107">DESCRIPTION</span></span>
<span data-ttu-id="39dd7-108">Cmdleten **Get-AzureRmManagedApplicationDefinition** hämtar definitioner för hanterade program</span><span class="sxs-lookup"><span data-stu-id="39dd7-108">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="39dd7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39dd7-109">EXAMPLES</span></span>

### <span data-ttu-id="39dd7-110">Exempel 1: Hämta alla definitioner för hanterade program under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="39dd7-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="39dd7-111">Det här kommandot hämtar definitionerna för hanterade program under resurs gruppen "MyRG"</span><span class="sxs-lookup"><span data-stu-id="39dd7-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="39dd7-112">Exempel 2: Hämta ett hanterat program</span><span class="sxs-lookup"><span data-stu-id="39dd7-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="39dd7-113">Det här kommandot får den hanterade program definitionen "myManagedAppDef" under resurs gruppen "MyRG"</span><span class="sxs-lookup"><span data-stu-id="39dd7-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="39dd7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39dd7-114">PARAMETERS</span></span>

### <span data-ttu-id="39dd7-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="39dd7-115">-ApiVersion</span></span>
<span data-ttu-id="39dd7-116">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="39dd7-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="39dd7-117">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="39dd7-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="39dd7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39dd7-118">-DefaultProfile</span></span>
<span data-ttu-id="39dd7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39dd7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39dd7-120">-ID</span><span class="sxs-lookup"><span data-stu-id="39dd7-120">-Id</span></span>
<span data-ttu-id="39dd7-121">Fullständigt kvalificerat ID för hanterade program, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="39dd7-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="39dd7-122">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="39dd7-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39dd7-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="39dd7-123">-Name</span></span>
<span data-ttu-id="39dd7-124">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="39dd7-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="39dd7-125">-För</span><span class="sxs-lookup"><span data-stu-id="39dd7-125">-Pre</span></span>
<span data-ttu-id="39dd7-126">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="39dd7-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="39dd7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39dd7-127">-ResourceGroupName</span></span>
<span data-ttu-id="39dd7-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="39dd7-128">The resource group name.</span></span>

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

### <span data-ttu-id="39dd7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39dd7-129">CommonParameters</span></span>
<span data-ttu-id="39dd7-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39dd7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39dd7-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39dd7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39dd7-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39dd7-132">INPUTS</span></span>

### <span data-ttu-id="39dd7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="39dd7-133">System.String</span></span>

## <span data-ttu-id="39dd7-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39dd7-134">OUTPUTS</span></span>

### <span data-ttu-id="39dd7-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="39dd7-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="39dd7-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39dd7-136">NOTES</span></span>

## <span data-ttu-id="39dd7-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39dd7-137">RELATED LINKS</span></span>
