---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: f81419f43defdf2c66d2d8f1768c63fc09ff0d35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916445"
---
# <span data-ttu-id="3a903-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="3a903-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="3a903-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3a903-102">SYNOPSIS</span></span>
<span data-ttu-id="3a903-103">Hämtar alla giltiga SKU: er som denna IotHub kan övergå till.</span><span class="sxs-lookup"><span data-stu-id="3a903-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="3a903-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3a903-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a903-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3a903-105">DESCRIPTION</span></span>
<span data-ttu-id="3a903-106">Hämtar alla giltiga SKU: er som den här IotHub kan övergå till.</span><span class="sxs-lookup"><span data-stu-id="3a903-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="3a903-107">En IotHub kan inte övergå mellan kostnads fria och betalda SKU: er och vice versa.</span><span class="sxs-lookup"><span data-stu-id="3a903-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="3a903-108">Du måste ta bort och återskapa iothub om du vill uppnå detta.</span><span class="sxs-lookup"><span data-stu-id="3a903-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="3a903-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3a903-109">EXAMPLES</span></span>

### <span data-ttu-id="3a903-110">Exempel 1 skaffa giltiga SKU: er</span><span class="sxs-lookup"><span data-stu-id="3a903-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="3a903-111">Hämtar en lista över alla SKU: er för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="3a903-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="3a903-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3a903-112">PARAMETERS</span></span>

### <span data-ttu-id="3a903-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a903-113">-DefaultProfile</span></span>
<span data-ttu-id="3a903-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3a903-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a903-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="3a903-115">-Name</span></span>
<span data-ttu-id="3a903-116">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3a903-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="3a903-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a903-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a903-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="3a903-118">Resource Group Name</span></span>

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

### <span data-ttu-id="3a903-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a903-119">CommonParameters</span></span>
<span data-ttu-id="3a903-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a903-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a903-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a903-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a903-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3a903-122">INPUTS</span></span>

### <span data-ttu-id="3a903-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3a903-123">System.String</span></span>

## <span data-ttu-id="3a903-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3a903-124">OUTPUTS</span></span>

### <span data-ttu-id="3a903-125">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="3a903-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="3a903-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3a903-126">NOTES</span></span>

## <span data-ttu-id="3a903-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3a903-127">RELATED LINKS</span></span>
