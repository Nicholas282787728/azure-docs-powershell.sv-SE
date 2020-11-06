---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 694f2ef459b50648e934e4ea0e434fe218d4b1f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581992"
---
# <span data-ttu-id="f8db6-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f8db6-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="f8db6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8db6-102">SYNOPSIS</span></span>
<span data-ttu-id="f8db6-103">Hämtar definitioner för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="f8db6-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8db6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8db6-104">SYNTAX</span></span>

### <span data-ttu-id="f8db6-105">GetBySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="f8db6-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8db6-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f8db6-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8db6-107">GetById</span><span class="sxs-lookup"><span data-stu-id="f8db6-107">GetById</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8db6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8db6-108">DESCRIPTION</span></span>
<span data-ttu-id="f8db6-109">Cmdleten **Get-AzureRmPolicySetDefinition** hämtar alla princip uppsättnings definitioner eller en specifik definition för princip uppsättning som identifieras med namn eller ID.</span><span class="sxs-lookup"><span data-stu-id="f8db6-109">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="f8db6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8db6-110">EXAMPLES</span></span>

### <span data-ttu-id="f8db6-111">Exempel 1: Hämta alla definitioner för princip uppsättningar</span><span class="sxs-lookup"><span data-stu-id="f8db6-111">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="f8db6-112">Det här kommandot får alla definitioner för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="f8db6-112">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="f8db6-113">Exempel 2: Hämta definition för princip uppsättning efter namn</span><span class="sxs-lookup"><span data-stu-id="f8db6-113">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="f8db6-114">Det här kommandot hämtar princip uppsättnings definitionen med namnet VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f8db6-114">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="f8db6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8db6-115">PARAMETERS</span></span>

### <span data-ttu-id="f8db6-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f8db6-116">-ApiVersion</span></span>
<span data-ttu-id="f8db6-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f8db6-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f8db6-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="f8db6-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f8db6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8db6-119">-DefaultProfile</span></span>
<span data-ttu-id="f8db6-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f8db6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8db6-121">-ID</span><span class="sxs-lookup"><span data-stu-id="f8db6-121">-Id</span></span>
<span data-ttu-id="f8db6-122">Det fullständiga kvalificerade princip uppsättningens Definitions-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f8db6-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="f8db6-123">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="f8db6-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8db6-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8db6-124">-Name</span></span>
<span data-ttu-id="f8db6-125">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="f8db6-125">The policy set definition name.</span></span>

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

### <span data-ttu-id="f8db6-126">-För</span><span class="sxs-lookup"><span data-stu-id="f8db6-126">-Pre</span></span>
<span data-ttu-id="f8db6-127">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f8db6-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f8db6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8db6-128">CommonParameters</span></span>
<span data-ttu-id="f8db6-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8db6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8db6-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8db6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8db6-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8db6-131">INPUTS</span></span>

### <span data-ttu-id="f8db6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f8db6-132">System.String</span></span>

## <span data-ttu-id="f8db6-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8db6-133">OUTPUTS</span></span>

### <span data-ttu-id="f8db6-134">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f8db6-134">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f8db6-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8db6-135">NOTES</span></span>

## <span data-ttu-id="f8db6-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8db6-136">RELATED LINKS</span></span>
