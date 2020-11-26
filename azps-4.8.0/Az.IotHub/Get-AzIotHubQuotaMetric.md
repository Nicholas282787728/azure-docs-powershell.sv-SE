---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259688"
---
# <span data-ttu-id="7f071-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="7f071-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="7f071-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f071-102">SYNOPSIS</span></span>
<span data-ttu-id="7f071-103">Hämtar kvot måtten för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="7f071-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="7f071-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f071-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f071-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f071-105">DESCRIPTION</span></span>
<span data-ttu-id="7f071-106">Hämtar kvot måtten för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="7f071-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="7f071-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f071-107">EXAMPLES</span></span>

### <span data-ttu-id="7f071-108">Exempel 1 Hämta kvot måtten</span><span class="sxs-lookup"><span data-stu-id="7f071-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="7f071-109">Hämtar kvot mått informationen för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="7f071-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7f071-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f071-110">PARAMETERS</span></span>

### <span data-ttu-id="7f071-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f071-111">-DefaultProfile</span></span>
<span data-ttu-id="7f071-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7f071-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f071-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="7f071-113">-Name</span></span>
<span data-ttu-id="7f071-114">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="7f071-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="7f071-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f071-115">-ResourceGroupName</span></span>
<span data-ttu-id="7f071-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7f071-116">Resource Group Name</span></span>

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

### <span data-ttu-id="7f071-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f071-117">CommonParameters</span></span>
<span data-ttu-id="7f071-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f071-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f071-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f071-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f071-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f071-120">INPUTS</span></span>

### <span data-ttu-id="7f071-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7f071-121">System.String</span></span>

## <span data-ttu-id="7f071-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f071-122">OUTPUTS</span></span>

### <span data-ttu-id="7f071-123">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="7f071-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="7f071-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f071-124">NOTES</span></span>

## <span data-ttu-id="7f071-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f071-125">RELATED LINKS</span></span>