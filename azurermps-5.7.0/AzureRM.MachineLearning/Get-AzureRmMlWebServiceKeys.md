---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: a0019b418fbf71a9b8010b4256a062a943244a9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578191"
---
# <span data-ttu-id="d9a79-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="d9a79-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="d9a79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9a79-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a79-103">Hämtar webb tjänstens nycklar.</span><span class="sxs-lookup"><span data-stu-id="d9a79-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9a79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9a79-104">SYNTAX</span></span>

### <span data-ttu-id="d9a79-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d9a79-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9a79-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="d9a79-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9a79-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9a79-107">DESCRIPTION</span></span>
<span data-ttu-id="d9a79-108">Hämtar snabb tangenterna för Azure Machine Learning Web Services API för körning.</span><span class="sxs-lookup"><span data-stu-id="d9a79-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="d9a79-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9a79-109">EXAMPLES</span></span>

### <span data-ttu-id="d9a79-110">--------------------------Exempel 1-hämta nycklar för en webb tjänst som anges av resurs grupp och namn--------------------------</span><span class="sxs-lookup"><span data-stu-id="d9a79-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="d9a79-111">--------------------------Exempel 2-hämta nycklar för webb tjänst instans--------------------------</span><span class="sxs-lookup"><span data-stu-id="d9a79-111">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="d9a79-112">$mlService är ett objekt av typen Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="d9a79-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="d9a79-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9a79-113">PARAMETERS</span></span>

### <span data-ttu-id="d9a79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a79-114">-DefaultProfile</span></span>
<span data-ttu-id="d9a79-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d9a79-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9a79-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="d9a79-116">-MlWebService</span></span>
<span data-ttu-id="d9a79-117">Namnet på webb tjänsten där åtkomst nycklar hämtas.</span><span class="sxs-lookup"><span data-stu-id="d9a79-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: WebService
Parameter Sets: GetByInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a79-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9a79-118">-Name</span></span>
<span data-ttu-id="d9a79-119">Namnet på webb tjänsten där åtkomst nycklar hämtas.</span><span class="sxs-lookup"><span data-stu-id="d9a79-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a79-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9a79-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9a79-121">Resurs gruppen för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d9a79-121">The resource group for the web service.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a79-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a79-122">CommonParameters</span></span>
<span data-ttu-id="d9a79-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9a79-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a79-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9a79-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a79-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9a79-125">INPUTS</span></span>

### <span data-ttu-id="d9a79-126">Webb tjänst</span><span class="sxs-lookup"><span data-stu-id="d9a79-126">WebService</span></span>
<span data-ttu-id="d9a79-127">Parametern ' MlWebService ' godkänner värdet för typen "WebService" från pipeline</span><span class="sxs-lookup"><span data-stu-id="d9a79-127">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="d9a79-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9a79-128">OUTPUTS</span></span>

### <span data-ttu-id="d9a79-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="d9a79-129">None</span></span>

## <span data-ttu-id="d9a79-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9a79-130">NOTES</span></span>
<span data-ttu-id="d9a79-131">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="d9a79-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d9a79-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9a79-132">RELATED LINKS</span></span>

