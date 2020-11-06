---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 12d809ad4c1df021891ab5acf384415d64aa08a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582579"
---
# <span data-ttu-id="1292c-101">New-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1292c-101">New-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="1292c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1292c-102">SYNOPSIS</span></span>
<span data-ttu-id="1292c-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="1292c-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1292c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1292c-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicyDefinition -Name <String> [-Description <String>]
 [-ServiceResource <System.Collections.Generic.List`1[System.String]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1292c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1292c-105">DESCRIPTION</span></span>
<span data-ttu-id="1292c-106">**New-AzureRmServiceEndpointPolicyDefinition-** cmdleten skapa en princip definition för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="1292c-106">The **New-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="1292c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1292c-107">EXAMPLES</span></span>

### <span data-ttu-id="1292c-108">Exempel 1: skapar en policy för tjänst slut punkter</span><span class="sxs-lookup"><span data-stu-id="1292c-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="1292c-109">Det här kommandot skapar princip definitionen för tjänste slut punkten med namnet ServiceEndpointPolicyDefinition1, service Microsoft. Storage, tjänst resurser prenumerationer/sub1 och beskrivning "ny definition" som tillhör resurs gruppen som heter ResourceGroup01 och lagrar den i $policydef variabeln.</span><span class="sxs-lookup"><span data-stu-id="1292c-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="1292c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1292c-110">PARAMETERS</span></span>

### <span data-ttu-id="1292c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1292c-111">-DefaultProfile</span></span>
<span data-ttu-id="1292c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1292c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1292c-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="1292c-113">-Description</span></span>
<span data-ttu-id="1292c-114">Beskrivning av definitionen</span><span class="sxs-lookup"><span data-stu-id="1292c-114">The description of the definition</span></span>

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

### <span data-ttu-id="1292c-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="1292c-115">-Name</span></span>
<span data-ttu-id="1292c-116">Namnet på tjänstens slut punkts princip</span><span class="sxs-lookup"><span data-stu-id="1292c-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="1292c-117">-Service</span><span class="sxs-lookup"><span data-stu-id="1292c-117">-Service</span></span>
<span data-ttu-id="1292c-118">Namn på tjänsten</span><span class="sxs-lookup"><span data-stu-id="1292c-118">Name of the service</span></span>

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

### <span data-ttu-id="1292c-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="1292c-119">-ServiceResource</span></span>
<span data-ttu-id="1292c-120">Lista över tjänst resurser</span><span class="sxs-lookup"><span data-stu-id="1292c-120">List of service resources</span></span>

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

### <span data-ttu-id="1292c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1292c-121">CommonParameters</span></span>
<span data-ttu-id="1292c-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1292c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1292c-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1292c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1292c-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1292c-124">INPUTS</span></span>

### <span data-ttu-id="1292c-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="1292c-125">None</span></span>


## <span data-ttu-id="1292c-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1292c-126">OUTPUTS</span></span>

### <span data-ttu-id="1292c-127">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1292c-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>


## <span data-ttu-id="1292c-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1292c-128">NOTES</span></span>

## <span data-ttu-id="1292c-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1292c-129">RELATED LINKS</span></span>
