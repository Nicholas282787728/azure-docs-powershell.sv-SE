---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 953a810585550ec8895fc9306f78633beb4846a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574535"
---
# <span data-ttu-id="e406c-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="e406c-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="e406c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e406c-102">SYNOPSIS</span></span>
<span data-ttu-id="e406c-103">Hämtar hanterade program</span><span class="sxs-lookup"><span data-stu-id="e406c-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e406c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e406c-104">SYNTAX</span></span>

### <span data-ttu-id="e406c-105">Parametern lista alla hanterade program.</span><span class="sxs-lookup"><span data-stu-id="e406c-105">The list all managed applications parameter set.</span></span> <span data-ttu-id="e406c-106">Vis</span><span class="sxs-lookup"><span data-stu-id="e406c-106">(Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e406c-107">Parametern för hanterade program namn.</span><span class="sxs-lookup"><span data-stu-id="e406c-107">The managed application name parameter set.</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e406c-108">Parametern hanterad program-ID.</span><span class="sxs-lookup"><span data-stu-id="e406c-108">The managed application Id parameter set.</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e406c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e406c-109">DESCRIPTION</span></span>
<span data-ttu-id="e406c-110">Cmdleten **Get-AzureRmManagedApplication** hämtar hanterade program</span><span class="sxs-lookup"><span data-stu-id="e406c-110">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="e406c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e406c-111">EXAMPLES</span></span>

### <span data-ttu-id="e406c-112">Exempel 1: Hämta alla hanterade program under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="e406c-112">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="e406c-113">Det här kommandot hämtar hanterade program under resurs gruppen "MyRG"</span><span class="sxs-lookup"><span data-stu-id="e406c-113">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="e406c-114">Exempel 2: Hämta alla hanterade program</span><span class="sxs-lookup"><span data-stu-id="e406c-114">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="e406c-115">Det här kommandot Hämta alla hanterade program under den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="e406c-115">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="e406c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e406c-116">PARAMETERS</span></span>

### <span data-ttu-id="e406c-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e406c-117">-ApiVersion</span></span>
<span data-ttu-id="e406c-118">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e406c-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e406c-119">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="e406c-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e406c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e406c-120">-DefaultProfile</span></span>
<span data-ttu-id="e406c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e406c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e406c-122">-ID</span><span class="sxs-lookup"><span data-stu-id="e406c-122">-Id</span></span>
<span data-ttu-id="e406c-123">Fullständigt kvalificerat program-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e406c-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="e406c-124">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="e406c-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e406c-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="e406c-125">-Name</span></span>
<span data-ttu-id="e406c-126">Namnet på det hanterade programmet.</span><span class="sxs-lookup"><span data-stu-id="e406c-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e406c-127">-För</span><span class="sxs-lookup"><span data-stu-id="e406c-127">-Pre</span></span>
<span data-ttu-id="e406c-128">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e406c-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e406c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e406c-129">-ResourceGroupName</span></span>
<span data-ttu-id="e406c-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e406c-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e406c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e406c-131">CommonParameters</span></span>
<span data-ttu-id="e406c-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e406c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e406c-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e406c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e406c-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e406c-134">INPUTS</span></span>

### <span data-ttu-id="e406c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e406c-135">System.String</span></span>

## <span data-ttu-id="e406c-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e406c-136">OUTPUTS</span></span>

### <span data-ttu-id="e406c-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e406c-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e406c-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e406c-138">NOTES</span></span>

## <span data-ttu-id="e406c-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e406c-139">RELATED LINKS</span></span>

