---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 9dec17ba09bf76ec7e8f3323b7cfd0557e08e525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582000"
---
# <span data-ttu-id="10160-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="10160-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="10160-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10160-102">SYNOPSIS</span></span>
<span data-ttu-id="10160-103">Hämtar definitioner för hanterade program</span><span class="sxs-lookup"><span data-stu-id="10160-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10160-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10160-104">SYNTAX</span></span>

### <span data-ttu-id="10160-105">GetByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="10160-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10160-106">GetById</span><span class="sxs-lookup"><span data-stu-id="10160-106">GetById</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10160-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10160-107">DESCRIPTION</span></span>
<span data-ttu-id="10160-108">Cmdleten **Get-AzureRmManagedApplicationDefinition** hämtar definitioner för hanterade program</span><span class="sxs-lookup"><span data-stu-id="10160-108">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="10160-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10160-109">EXAMPLES</span></span>

### <span data-ttu-id="10160-110">Exempel 1: Hämta alla definitioner för hanterade program under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="10160-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="10160-111">Det här kommandot hämtar definitionerna för hanterade program under resurs gruppen "MyRG"</span><span class="sxs-lookup"><span data-stu-id="10160-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="10160-112">Exempel 2: Hämta ett hanterat program</span><span class="sxs-lookup"><span data-stu-id="10160-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="10160-113">Det här kommandot får den hanterade program definitionen "myManagedAppDef" under resurs gruppen "MyRG"</span><span class="sxs-lookup"><span data-stu-id="10160-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="10160-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10160-114">PARAMETERS</span></span>

### <span data-ttu-id="10160-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="10160-115">-ApiVersion</span></span>
<span data-ttu-id="10160-116">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="10160-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="10160-117">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="10160-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="10160-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10160-118">-DefaultProfile</span></span>
<span data-ttu-id="10160-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10160-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10160-120">-ID</span><span class="sxs-lookup"><span data-stu-id="10160-120">-Id</span></span>
<span data-ttu-id="10160-121">Fullständigt kvalificerat ID för hanterade program, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="10160-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="10160-122">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="10160-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="10160-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="10160-123">-Name</span></span>
<span data-ttu-id="10160-124">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="10160-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="10160-125">-För</span><span class="sxs-lookup"><span data-stu-id="10160-125">-Pre</span></span>
<span data-ttu-id="10160-126">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="10160-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="10160-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10160-127">-ResourceGroupName</span></span>
<span data-ttu-id="10160-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="10160-128">The resource group name.</span></span>

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

### <span data-ttu-id="10160-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10160-129">CommonParameters</span></span>
<span data-ttu-id="10160-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10160-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10160-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10160-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10160-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10160-132">INPUTS</span></span>

### <span data-ttu-id="10160-133">System. String</span><span class="sxs-lookup"><span data-stu-id="10160-133">System.String</span></span>

## <span data-ttu-id="10160-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10160-134">OUTPUTS</span></span>

### <span data-ttu-id="10160-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="10160-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="10160-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10160-136">NOTES</span></span>

## <span data-ttu-id="10160-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10160-137">RELATED LINKS</span></span>
