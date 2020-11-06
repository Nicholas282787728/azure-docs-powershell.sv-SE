---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 14fbb8631a15321df9ae6834456649d00caae897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585491"
---
# <span data-ttu-id="0156b-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="0156b-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="0156b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0156b-102">SYNOPSIS</span></span>
<span data-ttu-id="0156b-103">Hämtar den sammanfattande informationen för en eller flera webb tjänster.</span><span class="sxs-lookup"><span data-stu-id="0156b-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0156b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0156b-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0156b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0156b-105">DESCRIPTION</span></span>
<span data-ttu-id="0156b-106">Hämtar information om webb tjänst defintion.</span><span class="sxs-lookup"><span data-stu-id="0156b-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="0156b-107">Beroende på vilken paramenters som skickas returnerar cmdleten defintion för en specifik webb tjänst, en samling defintions för webb tjänsterna för en viss resurs grupp i den aktuella prenumerationen eller en uppsättning defintions för webb tjänsterna i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0156b-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="0156b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0156b-108">EXAMPLES</span></span>

### <span data-ttu-id="0156b-109">--------------------------Exempel 1: få information om specifika webb tjänst--------------------------</span><span class="sxs-lookup"><span data-stu-id="0156b-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
<span data-ttu-id="0156b-110">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="0156b-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="0156b-111">--------------------------Exempel 2: Hämta alla webb tjänst resurser i aktuell prenumeration--------------------------</span><span class="sxs-lookup"><span data-stu-id="0156b-111">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
<span data-ttu-id="0156b-112">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="0156b-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService
```

### <span data-ttu-id="0156b-113">--------------------------Exempel 3: Hämta alla webb tjänster i det aktuella abonnemanget och resurs gruppen--------------------------</span><span class="sxs-lookup"><span data-stu-id="0156b-113">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="0156b-114">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="0156b-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="0156b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0156b-115">PARAMETERS</span></span>

### <span data-ttu-id="0156b-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0156b-116">-Name</span></span>
<span data-ttu-id="0156b-117">Namnet på webb tjänsten där informationen hämtas.</span><span class="sxs-lookup"><span data-stu-id="0156b-117">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="0156b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0156b-118">-ResourceGroupName</span></span>
<span data-ttu-id="0156b-119">Resurs gruppen som informationen för webb tjänsten hämtas från.</span><span class="sxs-lookup"><span data-stu-id="0156b-119">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="0156b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0156b-120">-DefaultProfile</span></span>
<span data-ttu-id="0156b-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0156b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0156b-122">-Region</span><span class="sxs-lookup"><span data-stu-id="0156b-122">-Region</span></span>
<span data-ttu-id="0156b-123">Namn på region</span><span class="sxs-lookup"><span data-stu-id="0156b-123">The name of region</span></span>

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

### <span data-ttu-id="0156b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0156b-124">CommonParameters</span></span>
<span data-ttu-id="0156b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0156b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0156b-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0156b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0156b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0156b-127">INPUTS</span></span>

## <span data-ttu-id="0156b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0156b-128">OUTPUTS</span></span>

### <span data-ttu-id="0156b-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="0156b-129">None</span></span>

## <span data-ttu-id="0156b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0156b-130">NOTES</span></span>
<span data-ttu-id="0156b-131">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="0156b-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0156b-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0156b-132">RELATED LINKS</span></span>

