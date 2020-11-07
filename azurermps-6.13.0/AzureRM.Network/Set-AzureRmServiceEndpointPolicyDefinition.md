---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 1348eff2e4a2ac755ac0f425ddb29816438199b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756144"
---
# <span data-ttu-id="fee75-101">Set-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fee75-101">Set-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="fee75-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fee75-102">SYNOPSIS</span></span>
<span data-ttu-id="fee75-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="fee75-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fee75-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fee75-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fee75-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fee75-105">DESCRIPTION</span></span>
<span data-ttu-id="fee75-106">Cmdleten **set-AzureRmServiceEndpointPolicyDefinition** skapa en princip definition för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="fee75-106">The **Set-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="fee75-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fee75-107">EXAMPLES</span></span>

### <span data-ttu-id="fee75-108">Exempel 1: uppdaterar en princip definition för tjänste slut punkter i en policy för tjänst slut punkter</span><span class="sxs-lookup"><span data-stu-id="fee75-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="fee75-109">Det här kommandot uppdaterar en princip definition för tjänste slut punkter med namnet Policydef1 i policyn för tjänste slut punkter som definieras av objektet $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="fee75-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="fee75-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fee75-110">PARAMETERS</span></span>

### <span data-ttu-id="fee75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee75-111">-DefaultProfile</span></span>
<span data-ttu-id="fee75-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fee75-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fee75-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="fee75-113">-Description</span></span>
<span data-ttu-id="fee75-114">Beskrivning av definitionen</span><span class="sxs-lookup"><span data-stu-id="fee75-114">The description of the definition</span></span>

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

### <span data-ttu-id="fee75-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="fee75-115">-Name</span></span>
<span data-ttu-id="fee75-116">Namnet på regeln</span><span class="sxs-lookup"><span data-stu-id="fee75-116">The name of the rule</span></span>

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

### <span data-ttu-id="fee75-117">-Service</span><span class="sxs-lookup"><span data-stu-id="fee75-117">-Service</span></span>
<span data-ttu-id="fee75-118">Namn på tjänsten</span><span class="sxs-lookup"><span data-stu-id="fee75-118">Name of the service</span></span>

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

### <span data-ttu-id="fee75-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fee75-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="fee75-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fee75-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="fee75-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="fee75-121">-ServiceResource</span></span>
<span data-ttu-id="fee75-122">Lista över tjänst resurser</span><span class="sxs-lookup"><span data-stu-id="fee75-122">List of service resources</span></span>

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

### <span data-ttu-id="fee75-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee75-123">CommonParameters</span></span>
<span data-ttu-id="fee75-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee75-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fee75-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fee75-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee75-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fee75-126">INPUTS</span></span>

### <span data-ttu-id="fee75-127">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fee75-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="fee75-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fee75-128">OUTPUTS</span></span>

### <span data-ttu-id="fee75-129">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fee75-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="fee75-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fee75-130">NOTES</span></span>

## <span data-ttu-id="fee75-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fee75-131">RELATED LINKS</span></span>
