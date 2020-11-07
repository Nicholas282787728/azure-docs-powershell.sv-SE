---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: 1de2d49d6e914635f8fc0d38ffa81755cc622481
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757622"
---
# <span data-ttu-id="f5c6a-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="f5c6a-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="f5c6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c6a-103">Hämtar kvot måtten för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="f5c6a-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5c6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5c6a-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5c6a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5c6a-105">DESCRIPTION</span></span>
<span data-ttu-id="f5c6a-106">Hämtar kvot måtten för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="f5c6a-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="f5c6a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5c6a-107">EXAMPLES</span></span>

### <span data-ttu-id="f5c6a-108">Exempel 1 Hämta kvot måtten</span><span class="sxs-lookup"><span data-stu-id="f5c6a-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f5c6a-109">Hämtar kvot mått informationen för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="f5c6a-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f5c6a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5c6a-110">PARAMETERS</span></span>

### <span data-ttu-id="f5c6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c6a-111">-DefaultProfile</span></span>
<span data-ttu-id="f5c6a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f5c6a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5c6a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="f5c6a-113">-Name</span></span>
<span data-ttu-id="f5c6a-114">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="f5c6a-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="f5c6a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5c6a-115">-ResourceGroupName</span></span>
<span data-ttu-id="f5c6a-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="f5c6a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f5c6a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c6a-117">CommonParameters</span></span>
<span data-ttu-id="f5c6a-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5c6a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c6a-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5c6a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c6a-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5c6a-120">INPUTS</span></span>

### <span data-ttu-id="f5c6a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f5c6a-121">System.String</span></span>

## <span data-ttu-id="f5c6a-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5c6a-122">OUTPUTS</span></span>

### <span data-ttu-id="f5c6a-123">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="f5c6a-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="f5c6a-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5c6a-124">NOTES</span></span>

## <span data-ttu-id="f5c6a-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5c6a-125">RELATED LINKS</span></span>