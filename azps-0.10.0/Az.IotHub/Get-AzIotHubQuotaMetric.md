---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 7da36f401647a4e020097eb2cfe6690aa1327755
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922798"
---
# <span data-ttu-id="bead9-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="bead9-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="bead9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bead9-102">SYNOPSIS</span></span>
<span data-ttu-id="bead9-103">Hämtar kvot måtten för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="bead9-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="bead9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bead9-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bead9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bead9-105">DESCRIPTION</span></span>
<span data-ttu-id="bead9-106">Hämtar kvot måtten för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="bead9-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="bead9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bead9-107">EXAMPLES</span></span>

### <span data-ttu-id="bead9-108">Exempel 1 Hämta kvot måtten</span><span class="sxs-lookup"><span data-stu-id="bead9-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="bead9-109">Hämtar kvot mått informationen för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="bead9-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="bead9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bead9-110">PARAMETERS</span></span>

### <span data-ttu-id="bead9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bead9-111">-DefaultProfile</span></span>
<span data-ttu-id="bead9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bead9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bead9-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="bead9-113">-Name</span></span>
<span data-ttu-id="bead9-114">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="bead9-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="bead9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bead9-115">-ResourceGroupName</span></span>
<span data-ttu-id="bead9-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="bead9-116">Resource Group Name</span></span>

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

### <span data-ttu-id="bead9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bead9-117">CommonParameters</span></span>
<span data-ttu-id="bead9-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bead9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bead9-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bead9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bead9-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bead9-120">INPUTS</span></span>

### <span data-ttu-id="bead9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="bead9-121">System.String</span></span>

## <span data-ttu-id="bead9-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bead9-122">OUTPUTS</span></span>

### <span data-ttu-id="bead9-123">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="bead9-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="bead9-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bead9-124">NOTES</span></span>

## <span data-ttu-id="bead9-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bead9-125">RELATED LINKS</span></span>
