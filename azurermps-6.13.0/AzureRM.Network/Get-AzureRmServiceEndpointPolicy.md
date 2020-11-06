---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 989b6aa91c0dabec1b72425f214c4097df374041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575212"
---
# <span data-ttu-id="ca89a-101">Get-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ca89a-101">Get-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="ca89a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca89a-102">SYNOPSIS</span></span>
<span data-ttu-id="ca89a-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="ca89a-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca89a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca89a-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca89a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca89a-105">DESCRIPTION</span></span>
<span data-ttu-id="ca89a-106">Cmdleten **Get-AzureRmServiceEndpointPolicy** hämtar en policy för tjänst slut punkter.</span><span class="sxs-lookup"><span data-stu-id="ca89a-106">The **Get-AzureRmServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="ca89a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca89a-107">EXAMPLES</span></span>

### <span data-ttu-id="ca89a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ca89a-108">Example 1</span></span>
```
$policy = Get-AzureRmServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ca89a-109">Det här kommandot hämtar tjänste slut punkts principen med namnet ServiceEndpointPolicy1 som tillhör resurs gruppen som heter ResourceGroup01 och lagrar den i $policy variabel.</span><span class="sxs-lookup"><span data-stu-id="ca89a-109">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="ca89a-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ca89a-110">Example 2</span></span>
```
$policyList = Get-AzureRmServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ca89a-111">Det här kommandot får en lista över alla tjänste slut punkts principer i resurs gruppen som heter ResourceGroup01 och lagrar den i $policyList variabeln.</span><span class="sxs-lookup"><span data-stu-id="ca89a-111">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

## <span data-ttu-id="ca89a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca89a-112">PARAMETERS</span></span>

### <span data-ttu-id="ca89a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca89a-113">-DefaultProfile</span></span>
<span data-ttu-id="ca89a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca89a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca89a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca89a-115">-Name</span></span>
<span data-ttu-id="ca89a-116">Namnet på tjänstens slut punkts princip</span><span class="sxs-lookup"><span data-stu-id="ca89a-116">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca89a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca89a-117">-ResourceGroupName</span></span>
<span data-ttu-id="ca89a-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ca89a-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca89a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca89a-119">CommonParameters</span></span>
<span data-ttu-id="ca89a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca89a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ca89a-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca89a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca89a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca89a-122">INPUTS</span></span>

### <span data-ttu-id="ca89a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ca89a-123">System.String</span></span>


## <span data-ttu-id="ca89a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca89a-124">OUTPUTS</span></span>

### <span data-ttu-id="ca89a-125">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ca89a-125">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="ca89a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca89a-126">NOTES</span></span>

## <span data-ttu-id="ca89a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca89a-127">RELATED LINKS</span></span>
