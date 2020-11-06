---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 7d0df70118f50274ccecfd730e752efabcf52519
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576937"
---
# <span data-ttu-id="a554e-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="a554e-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="a554e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a554e-102">SYNOPSIS</span></span>
<span data-ttu-id="a554e-103">Hämtar webb tjänstens nycklar.</span><span class="sxs-lookup"><span data-stu-id="a554e-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a554e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a554e-104">SYNTAX</span></span>

### <span data-ttu-id="a554e-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a554e-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a554e-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="a554e-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a554e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a554e-107">DESCRIPTION</span></span>
<span data-ttu-id="a554e-108">Hämtar snabb tangenterna för Azure Machine Learning Web Services API för körning.</span><span class="sxs-lookup"><span data-stu-id="a554e-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="a554e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a554e-109">EXAMPLES</span></span>

### <span data-ttu-id="a554e-110">Exempel 1-hämta nycklar för en webb tjänst som anges av resurs grupp och namn</span><span class="sxs-lookup"><span data-stu-id="a554e-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="a554e-111">Exempel 2 – hämta nycklar för webb tjänst instans</span><span class="sxs-lookup"><span data-stu-id="a554e-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="a554e-112">$mlService är ett objekt av typen Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="a554e-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="a554e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a554e-113">PARAMETERS</span></span>

### <span data-ttu-id="a554e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a554e-114">-DefaultProfile</span></span>
<span data-ttu-id="a554e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a554e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a554e-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="a554e-116">-MlWebService</span></span>
<span data-ttu-id="a554e-117">Namnet på webb tjänsten där åtkomst nycklar hämtas.</span><span class="sxs-lookup"><span data-stu-id="a554e-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="a554e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="a554e-118">-Name</span></span>
<span data-ttu-id="a554e-119">Namnet på webb tjänsten där åtkomst nycklar hämtas.</span><span class="sxs-lookup"><span data-stu-id="a554e-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="a554e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a554e-120">-ResourceGroupName</span></span>
<span data-ttu-id="a554e-121">Resurs gruppen för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a554e-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="a554e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a554e-122">CommonParameters</span></span>
<span data-ttu-id="a554e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a554e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a554e-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a554e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a554e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a554e-125">INPUTS</span></span>

### <span data-ttu-id="a554e-126">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="a554e-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="a554e-127">Parametrar: MlWebService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a554e-127">Parameters: MlWebService (ByValue)</span></span>

## <span data-ttu-id="a554e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a554e-128">OUTPUTS</span></span>

### <span data-ttu-id="a554e-129">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="a554e-129">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="a554e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a554e-130">NOTES</span></span>
<span data-ttu-id="a554e-131">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="a554e-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a554e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a554e-132">RELATED LINKS</span></span>
