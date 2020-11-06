---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 694ac928d78cf64f500730c57e394a8e3a425456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585483"
---
# <span data-ttu-id="60cf8-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="60cf8-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="60cf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="60cf8-103">Hämtar webb tjänstens nycklar.</span><span class="sxs-lookup"><span data-stu-id="60cf8-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60cf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60cf8-104">SYNTAX</span></span>

### <span data-ttu-id="60cf8-105">Skaffa en Azure ML webb tjänsts åtkomst nycklar med namn och resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="60cf8-105">Get an Azure ML web service's access keys given its name and resource group.</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60cf8-106">Hämta Access-kesy för den angivna webb tjänst instansen.</span><span class="sxs-lookup"><span data-stu-id="60cf8-106">Get the access kesy for the given web service instance.</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60cf8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60cf8-107">DESCRIPTION</span></span>
<span data-ttu-id="60cf8-108">Hämtar snabb tangenterna för Azure Machine Learning Web Services API för körning.</span><span class="sxs-lookup"><span data-stu-id="60cf8-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="60cf8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60cf8-109">EXAMPLES</span></span>

### <span data-ttu-id="60cf8-110">--------------------------Exempel 1-hämta nycklar för en webb tjänst som anges av resurs grupp och namn--------------------------</span><span class="sxs-lookup"><span data-stu-id="60cf8-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
<span data-ttu-id="60cf8-111">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="60cf8-111">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="60cf8-112">--------------------------Exempel 2-hämta nycklar för webb tjänst instans--------------------------</span><span class="sxs-lookup"><span data-stu-id="60cf8-112">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
<span data-ttu-id="60cf8-113">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="60cf8-113">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="60cf8-114">$mlService är ett objekt av typen Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="60cf8-114">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="60cf8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60cf8-115">PARAMETERS</span></span>

### <span data-ttu-id="60cf8-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="60cf8-116">-MlWebService</span></span>
<span data-ttu-id="60cf8-117">Namnet på webb tjänsten där åtkomst nycklar hämtas.</span><span class="sxs-lookup"><span data-stu-id="60cf8-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Get the access kesy for the given web service instance.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60cf8-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="60cf8-118">-Name</span></span>
<span data-ttu-id="60cf8-119">Namnet på webb tjänsten där åtkomst nycklar hämtas.</span><span class="sxs-lookup"><span data-stu-id="60cf8-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cf8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60cf8-120">-ResourceGroupName</span></span>
<span data-ttu-id="60cf8-121">Resurs gruppen för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="60cf8-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cf8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60cf8-122">-DefaultProfile</span></span>
<span data-ttu-id="60cf8-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60cf8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60cf8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60cf8-124">CommonParameters</span></span>
<span data-ttu-id="60cf8-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60cf8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60cf8-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60cf8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60cf8-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60cf8-127">INPUTS</span></span>

### <span data-ttu-id="60cf8-128">Webb tjänst</span><span class="sxs-lookup"><span data-stu-id="60cf8-128">WebService</span></span>
<span data-ttu-id="60cf8-129">Parametern ' MlWebService ' godkänner värdet för typen "WebService" från pipeline</span><span class="sxs-lookup"><span data-stu-id="60cf8-129">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="60cf8-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60cf8-130">OUTPUTS</span></span>

### <span data-ttu-id="60cf8-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="60cf8-131">None</span></span>

## <span data-ttu-id="60cf8-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60cf8-132">NOTES</span></span>
<span data-ttu-id="60cf8-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="60cf8-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="60cf8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60cf8-134">RELATED LINKS</span></span>

