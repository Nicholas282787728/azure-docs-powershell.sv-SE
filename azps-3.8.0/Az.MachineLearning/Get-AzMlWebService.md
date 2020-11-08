---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: be34a81e28f2a11ed604afe922694872fedb5f0a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091970"
---
# <span data-ttu-id="e08ec-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="e08ec-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="e08ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e08ec-102">SYNOPSIS</span></span>
<span data-ttu-id="e08ec-103">Hämtar den sammanfattande informationen för en eller flera webb tjänster.</span><span class="sxs-lookup"><span data-stu-id="e08ec-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="e08ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e08ec-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e08ec-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e08ec-105">DESCRIPTION</span></span>
<span data-ttu-id="e08ec-106">Hämtar information om webb tjänst definitioner.</span><span class="sxs-lookup"><span data-stu-id="e08ec-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="e08ec-107">Beroende på vilka parametrar som skickas returnerar cmdleten definitionen för en specifik webb tjänst, en uppsättning definitioner för webb tjänsterna för en viss resurs grupp i den aktuella prenumerationen, eller en uppsättning definitioner för webb tjänsterna i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e08ec-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="e08ec-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e08ec-108">EXAMPLES</span></span>

### <span data-ttu-id="e08ec-109">Exempel 1: Hämta information om specifik webb tjänst</span><span class="sxs-lookup"><span data-stu-id="e08ec-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="e08ec-110">Exempel 2: Hämta alla webb tjänst resurser i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="e08ec-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="e08ec-111">Exempel 3: Hämta alla webb tjänster i det aktuella abonnemanget och resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e08ec-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="e08ec-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e08ec-112">PARAMETERS</span></span>

### <span data-ttu-id="e08ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e08ec-113">-DefaultProfile</span></span>
<span data-ttu-id="e08ec-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e08ec-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08ec-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e08ec-115">-Name</span></span>
<span data-ttu-id="e08ec-116">Namnet på webb tjänsten där informationen hämtas.</span><span class="sxs-lookup"><span data-stu-id="e08ec-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="e08ec-117">-Region</span><span class="sxs-lookup"><span data-stu-id="e08ec-117">-Region</span></span>
<span data-ttu-id="e08ec-118">Namn på region</span><span class="sxs-lookup"><span data-stu-id="e08ec-118">The name of region</span></span>

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

### <span data-ttu-id="e08ec-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e08ec-119">-ResourceGroupName</span></span>
<span data-ttu-id="e08ec-120">Resurs gruppen som informationen för webb tjänsten hämtas från.</span><span class="sxs-lookup"><span data-stu-id="e08ec-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="e08ec-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e08ec-121">CommonParameters</span></span>
<span data-ttu-id="e08ec-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e08ec-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e08ec-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e08ec-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e08ec-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e08ec-124">INPUTS</span></span>

### <span data-ttu-id="e08ec-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="e08ec-125">None</span></span>

## <span data-ttu-id="e08ec-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e08ec-126">OUTPUTS</span></span>

### <span data-ttu-id="e08ec-127">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="e08ec-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="e08ec-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e08ec-128">NOTES</span></span>
<span data-ttu-id="e08ec-129">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="e08ec-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e08ec-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e08ec-130">RELATED LINKS</span></span>