---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: ef724c4d2e9771243058471c3ce2aebc944d2bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755642"
---
# <span data-ttu-id="c3a60-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="c3a60-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="c3a60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3a60-102">SYNOPSIS</span></span>
<span data-ttu-id="c3a60-103">Hämtar definitioner för hanterade program</span><span class="sxs-lookup"><span data-stu-id="c3a60-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3a60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3a60-104">SYNTAX</span></span>

### <span data-ttu-id="c3a60-105">Parameter uppsättning för hanterade program namn.</span><span class="sxs-lookup"><span data-stu-id="c3a60-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="c3a60-106">Vis</span><span class="sxs-lookup"><span data-stu-id="c3a60-106">(Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3a60-107">Parameter uppsättning för definition av hanterade program.</span><span class="sxs-lookup"><span data-stu-id="c3a60-107">The managed application definition Id parameter set.</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3a60-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3a60-108">DESCRIPTION</span></span>
<span data-ttu-id="c3a60-109">Cmdleten **Get-AzureRmManagedApplicationDefinition** hämtar definitioner för hanterade program</span><span class="sxs-lookup"><span data-stu-id="c3a60-109">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="c3a60-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3a60-110">EXAMPLES</span></span>

### <span data-ttu-id="c3a60-111">Exempel 1: Hämta alla definitioner för hanterade program under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="c3a60-111">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="c3a60-112">Det här kommandot hämtar definitionerna för hanterade program under resurs gruppen "MyRG"</span><span class="sxs-lookup"><span data-stu-id="c3a60-112">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="c3a60-113">Exempel 2: Hämta ett hanterat program</span><span class="sxs-lookup"><span data-stu-id="c3a60-113">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="c3a60-114">Det här kommandot får den hanterade program definitionen "myManagedAppDef" under resurs gruppen "MyRG"</span><span class="sxs-lookup"><span data-stu-id="c3a60-114">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="c3a60-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3a60-115">PARAMETERS</span></span>

### <span data-ttu-id="c3a60-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c3a60-116">-ApiVersion</span></span>
<span data-ttu-id="c3a60-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c3a60-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c3a60-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="c3a60-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c3a60-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3a60-119">-DefaultProfile</span></span>
<span data-ttu-id="c3a60-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3a60-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3a60-121">-ID</span><span class="sxs-lookup"><span data-stu-id="c3a60-121">-Id</span></span>
<span data-ttu-id="c3a60-122">Fullständigt kvalificerat ID för hanterade program, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c3a60-122">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="c3a60-123">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="c3a60-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3a60-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3a60-124">-Name</span></span>
<span data-ttu-id="c3a60-125">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="c3a60-125">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3a60-126">-För</span><span class="sxs-lookup"><span data-stu-id="c3a60-126">-Pre</span></span>
<span data-ttu-id="c3a60-127">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c3a60-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c3a60-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3a60-128">-ResourceGroupName</span></span>
<span data-ttu-id="c3a60-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c3a60-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3a60-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3a60-130">CommonParameters</span></span>
<span data-ttu-id="c3a60-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3a60-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3a60-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3a60-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3a60-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3a60-133">INPUTS</span></span>

### <span data-ttu-id="c3a60-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c3a60-134">System.String</span></span>

## <span data-ttu-id="c3a60-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3a60-135">OUTPUTS</span></span>

### <span data-ttu-id="c3a60-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c3a60-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c3a60-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3a60-137">NOTES</span></span>

## <span data-ttu-id="c3a60-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3a60-138">RELATED LINKS</span></span>

