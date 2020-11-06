---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 802a3be7aca857b798f1e853bec499c5397b6e65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575628"
---
# <span data-ttu-id="e4b00-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="e4b00-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="e4b00-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4b00-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b00-103">Hämtar den sammanfattande informationen för en eller flera webb tjänster.</span><span class="sxs-lookup"><span data-stu-id="e4b00-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4b00-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4b00-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4b00-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4b00-105">DESCRIPTION</span></span>
<span data-ttu-id="e4b00-106">Hämtar information om webb tjänst defintion.</span><span class="sxs-lookup"><span data-stu-id="e4b00-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="e4b00-107">Beroende på vilken paramenters som skickas returnerar cmdleten defintion för en specifik webb tjänst, en samling defintions för webb tjänsterna för en viss resurs grupp i den aktuella prenumerationen eller en uppsättning defintions för webb tjänsterna i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e4b00-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="e4b00-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4b00-108">EXAMPLES</span></span>

### <span data-ttu-id="e4b00-109">--------------------------Exempel 1: få information om specifika webb tjänst--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4b00-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="e4b00-110">--------------------------Exempel 2: Hämta alla webb tjänst resurser i aktuell prenumeration--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4b00-110">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
```
Get-AzureRmMlWebService
```

### <span data-ttu-id="e4b00-111">--------------------------Exempel 3: Hämta alla webb tjänster i det aktuella abonnemanget och resurs gruppen--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4b00-111">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="e4b00-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4b00-112">PARAMETERS</span></span>

### <span data-ttu-id="e4b00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b00-113">-DefaultProfile</span></span>
<span data-ttu-id="e4b00-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e4b00-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4b00-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e4b00-115">-Name</span></span>
<span data-ttu-id="e4b00-116">Namnet på webb tjänsten där informationen hämtas.</span><span class="sxs-lookup"><span data-stu-id="e4b00-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="e4b00-117">-Region</span><span class="sxs-lookup"><span data-stu-id="e4b00-117">-Region</span></span>
<span data-ttu-id="e4b00-118">Namnet på Regio</span><span class="sxs-lookup"><span data-stu-id="e4b00-118">The name of regio</span></span>

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

### <span data-ttu-id="e4b00-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4b00-119">-ResourceGroupName</span></span>
<span data-ttu-id="e4b00-120">Resurs gruppen som informationen för webb tjänsten hämtas från.</span><span class="sxs-lookup"><span data-stu-id="e4b00-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="e4b00-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b00-121">CommonParameters</span></span>
<span data-ttu-id="e4b00-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4b00-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b00-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4b00-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b00-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4b00-124">INPUTS</span></span>

### <span data-ttu-id="e4b00-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="e4b00-125">None</span></span>
<span data-ttu-id="e4b00-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e4b00-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4b00-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4b00-127">OUTPUTS</span></span>

### <span data-ttu-id="e4b00-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="e4b00-128">None</span></span>

## <span data-ttu-id="e4b00-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4b00-129">NOTES</span></span>
<span data-ttu-id="e4b00-130">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="e4b00-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e4b00-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4b00-131">RELATED LINKS</span></span>

