---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: ac58450295e0e2d988c12c308c0210b38ad71b4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757059"
---
# <span data-ttu-id="338d0-101">Add-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="338d0-101">Add-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="338d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="338d0-102">SYNOPSIS</span></span>
<span data-ttu-id="338d0-103">Lägger till en princip definition för tjänste slut punkter till en angiven princip.</span><span class="sxs-lookup"><span data-stu-id="338d0-103">Adds a service endpoint policy definition to a specified policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="338d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="338d0-104">SYNTAX</span></span>

```
Add-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="338d0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="338d0-105">DESCRIPTION</span></span>
<span data-ttu-id="338d0-106">Cmdleten **Add-AzureRmServiceEndpointPolicyDefinition** lägger till en definition för tjänste slut punkter till principen.</span><span class="sxs-lookup"><span data-stu-id="338d0-106">The **Add-AzureRmServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="338d0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="338d0-107">EXAMPLES</span></span>

### <span data-ttu-id="338d0-108">Exempel 1: uppdaterar en princip definition för tjänste slut punkter i en policy för tjänst slut punkter</span><span class="sxs-lookup"><span data-stu-id="338d0-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="338d0-109">Det här kommandot uppdaterade policy definitionen för tjänste slut punkten med namnet ServiceEndpointPolicyDefinition1, service Microsoft. Storage, tjänst resurser prenumerationer/sub1 och beskrivning "ny definition" som tillhör resurs gruppen som heter ResourceGroup01 och lagrar den i $policydef variabeln.</span><span class="sxs-lookup"><span data-stu-id="338d0-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="338d0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="338d0-110">PARAMETERS</span></span>

### <span data-ttu-id="338d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="338d0-111">-DefaultProfile</span></span>
<span data-ttu-id="338d0-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="338d0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="338d0-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="338d0-113">-Description</span></span>
<span data-ttu-id="338d0-114">Beskrivning av definitionen</span><span class="sxs-lookup"><span data-stu-id="338d0-114">The description of the definition</span></span>

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

### <span data-ttu-id="338d0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="338d0-115">-Name</span></span>
<span data-ttu-id="338d0-116">Namnet på princip definitionen för tjänste slut punkten</span><span class="sxs-lookup"><span data-stu-id="338d0-116">The name of the service endpoint policy definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338d0-117">-Service</span><span class="sxs-lookup"><span data-stu-id="338d0-117">-Service</span></span>
<span data-ttu-id="338d0-118">Namn på tjänsten</span><span class="sxs-lookup"><span data-stu-id="338d0-118">Name of the service</span></span>

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

### <span data-ttu-id="338d0-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="338d0-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="338d0-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="338d0-120">The ServiceEndpointPolicy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="338d0-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="338d0-121">-ServiceResource</span></span>
<span data-ttu-id="338d0-122">Lista över tjänst resurser</span><span class="sxs-lookup"><span data-stu-id="338d0-122">List of service resources</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338d0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="338d0-123">CommonParameters</span></span>
<span data-ttu-id="338d0-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="338d0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="338d0-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="338d0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="338d0-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="338d0-126">INPUTS</span></span>

### <span data-ttu-id="338d0-127">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="338d0-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="338d0-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="338d0-128">OUTPUTS</span></span>

### <span data-ttu-id="338d0-129">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="338d0-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="338d0-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="338d0-130">NOTES</span></span>

## <span data-ttu-id="338d0-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="338d0-131">RELATED LINKS</span></span>
