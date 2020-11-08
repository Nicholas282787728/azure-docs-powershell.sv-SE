---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259387"
---
# <span data-ttu-id="f9c36-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="f9c36-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="f9c36-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9c36-102">SYNOPSIS</span></span>
<span data-ttu-id="f9c36-103">Hämtar webb tjänstens nycklar.</span><span class="sxs-lookup"><span data-stu-id="f9c36-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="f9c36-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9c36-104">SYNTAX</span></span>

### <span data-ttu-id="f9c36-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9c36-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9c36-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="f9c36-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9c36-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9c36-107">DESCRIPTION</span></span>
<span data-ttu-id="f9c36-108">Hämtar snabb tangenterna för Azure Machine Learning Web Services API för körning.</span><span class="sxs-lookup"><span data-stu-id="f9c36-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="f9c36-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9c36-109">EXAMPLES</span></span>

### <span data-ttu-id="f9c36-110">Exempel 1-hämta nycklar för en webb tjänst som anges av resurs grupp och namn</span><span class="sxs-lookup"><span data-stu-id="f9c36-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="f9c36-111">Exempel 2 – hämta nycklar för webb tjänst instans</span><span class="sxs-lookup"><span data-stu-id="f9c36-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="f9c36-112">$mlService är ett objekt av typen Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="f9c36-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="f9c36-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9c36-113">PARAMETERS</span></span>

### <span data-ttu-id="f9c36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9c36-114">-DefaultProfile</span></span>
<span data-ttu-id="f9c36-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f9c36-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9c36-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="f9c36-116">-MlWebService</span></span>
<span data-ttu-id="f9c36-117">Namnet på webb tjänsten där åtkomst nycklar hämtas.</span><span class="sxs-lookup"><span data-stu-id="f9c36-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: GetByInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9c36-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="f9c36-118">-Name</span></span>
<span data-ttu-id="f9c36-119">Namnet på webb tjänsten där åtkomst nycklar hämtas.</span><span class="sxs-lookup"><span data-stu-id="f9c36-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c36-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9c36-120">-ResourceGroupName</span></span>
<span data-ttu-id="f9c36-121">Resurs gruppen för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f9c36-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c36-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9c36-122">CommonParameters</span></span>
<span data-ttu-id="f9c36-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9c36-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9c36-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9c36-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9c36-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9c36-125">INPUTS</span></span>

### <span data-ttu-id="f9c36-126">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="f9c36-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="f9c36-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9c36-127">OUTPUTS</span></span>

### <span data-ttu-id="f9c36-128">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="f9c36-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="f9c36-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9c36-129">NOTES</span></span>
<span data-ttu-id="f9c36-130">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="f9c36-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f9c36-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9c36-131">RELATED LINKS</span></span>
