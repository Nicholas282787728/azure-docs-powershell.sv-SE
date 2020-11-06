---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 5fba45e50076952a0a2e11e2e5541ab9546d3bc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581352"
---
# <span data-ttu-id="25b65-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="25b65-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="25b65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25b65-102">SYNOPSIS</span></span>
<span data-ttu-id="25b65-103">Hämtar definitioner för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="25b65-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25b65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25b65-104">SYNTAX</span></span>

### <span data-ttu-id="25b65-105">Parametern lista alla definitioner för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="25b65-105">The list all policy set definitions parameter set.</span></span> <span data-ttu-id="25b65-106">Vis</span><span class="sxs-lookup"><span data-stu-id="25b65-106">(Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25b65-107">Parameter uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="25b65-107">The policy set definition name parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25b65-108">Parametern uppsättning med Definitions-ID för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="25b65-108">The policy set definition Id parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25b65-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25b65-109">DESCRIPTION</span></span>
<span data-ttu-id="25b65-110">Cmdleten **Get-AzureRmPolicySetDefinition** hämtar alla princip uppsättnings definitioner eller en specifik definition för princip uppsättning som identifieras med namn eller ID.</span><span class="sxs-lookup"><span data-stu-id="25b65-110">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="25b65-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25b65-111">EXAMPLES</span></span>

### <span data-ttu-id="25b65-112">Exempel 1: Hämta alla definitioner för princip uppsättningar</span><span class="sxs-lookup"><span data-stu-id="25b65-112">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="25b65-113">Det här kommandot får alla definitioner för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="25b65-113">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="25b65-114">Exempel 2: Hämta definition för princip uppsättning efter namn</span><span class="sxs-lookup"><span data-stu-id="25b65-114">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="25b65-115">Det här kommandot hämtar princip uppsättnings definitionen med namnet VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="25b65-115">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="25b65-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25b65-116">PARAMETERS</span></span>

### <span data-ttu-id="25b65-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="25b65-117">-ApiVersion</span></span>
<span data-ttu-id="25b65-118">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="25b65-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="25b65-119">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="25b65-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="25b65-120">-ID</span><span class="sxs-lookup"><span data-stu-id="25b65-120">-Id</span></span>
<span data-ttu-id="25b65-121">Det fullständiga kvalificerade princip uppsättningens Definitions-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="25b65-121">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="25b65-122">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="25b65-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b65-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="25b65-123">-Name</span></span>
<span data-ttu-id="25b65-124">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="25b65-124">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b65-125">-För</span><span class="sxs-lookup"><span data-stu-id="25b65-125">-Pre</span></span>
<span data-ttu-id="25b65-126">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="25b65-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="25b65-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b65-127">-DefaultProfile</span></span>
<span data-ttu-id="25b65-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25b65-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25b65-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b65-129">CommonParameters</span></span>
<span data-ttu-id="25b65-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b65-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b65-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25b65-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b65-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25b65-132">INPUTS</span></span>

### <span data-ttu-id="25b65-133">System. String</span><span class="sxs-lookup"><span data-stu-id="25b65-133">System.String</span></span>

## <span data-ttu-id="25b65-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25b65-134">OUTPUTS</span></span>

### <span data-ttu-id="25b65-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="25b65-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="25b65-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25b65-136">NOTES</span></span>

## <span data-ttu-id="25b65-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25b65-137">RELATED LINKS</span></span>

