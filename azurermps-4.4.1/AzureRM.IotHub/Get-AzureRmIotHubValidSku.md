---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
ms.openlocfilehash: 904fb627be4460fbbca0dc6dae9a68fc0dd468ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584719"
---
# <span data-ttu-id="15eb6-101">Get-AzureRmIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="15eb6-101">Get-AzureRmIotHubValidSku</span></span>

## <span data-ttu-id="15eb6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="15eb6-103">Hämtar alla giltiga SKU: er som denna IotHub kan övergå till.</span><span class="sxs-lookup"><span data-stu-id="15eb6-103">Gets all valid skus that this IotHub can transition to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15eb6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15eb6-104">SYNTAX</span></span>

```
Get-AzureRmIotHubValidSku [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15eb6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="15eb6-106">Hämtar alla giltiga SKU: er som den här IotHub kan övergå till.</span><span class="sxs-lookup"><span data-stu-id="15eb6-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="15eb6-107">En IotHub kan inte övergå mellan kostnads fria och betalda SKU: er och vice versa.</span><span class="sxs-lookup"><span data-stu-id="15eb6-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="15eb6-108">Du måste ta bort och återskapa iothub om du vill uppnå detta.</span><span class="sxs-lookup"><span data-stu-id="15eb6-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="15eb6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15eb6-109">EXAMPLES</span></span>

### <span data-ttu-id="15eb6-110">Exempel 1 skaffa giltiga SKU: er</span><span class="sxs-lookup"><span data-stu-id="15eb6-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzureRmIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="15eb6-111">Hämtar en lista över alla SKU: er för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="15eb6-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="15eb6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15eb6-112">PARAMETERS</span></span>

### <span data-ttu-id="15eb6-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="15eb6-113">-Name</span></span>
<span data-ttu-id="15eb6-114">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="15eb6-114">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15eb6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15eb6-115">-ResourceGroupName</span></span>
<span data-ttu-id="15eb6-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="15eb6-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15eb6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15eb6-117">-DefaultProfile</span></span>
<span data-ttu-id="15eb6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15eb6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15eb6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15eb6-119">CommonParameters</span></span>
<span data-ttu-id="15eb6-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15eb6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15eb6-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15eb6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15eb6-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15eb6-122">INPUTS</span></span>

### <span data-ttu-id="15eb6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="15eb6-123">System.String</span></span>

## <span data-ttu-id="15eb6-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15eb6-124">OUTPUTS</span></span>

### <span data-ttu-id="15eb6-125">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubSkuDescription, Microsoft. Azure. commands. IotHub, version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="15eb6-125">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="15eb6-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15eb6-126">NOTES</span></span>

## <span data-ttu-id="15eb6-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15eb6-127">RELATED LINKS</span></span>

