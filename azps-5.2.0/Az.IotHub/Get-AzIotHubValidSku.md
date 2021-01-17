---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: e0f178c10fa74d8fa230472397d7bcc835f98bf4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417120"
---
# <span data-ttu-id="e056a-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="e056a-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="e056a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e056a-102">SYNOPSIS</span></span>
<span data-ttu-id="e056a-103">Hämtar alla giltiga SKU: er som denna IotHub kan övergå till.</span><span class="sxs-lookup"><span data-stu-id="e056a-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="e056a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e056a-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e056a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e056a-105">DESCRIPTION</span></span>
<span data-ttu-id="e056a-106">Hämtar alla giltiga SKU: er som den här IotHub kan övergå till.</span><span class="sxs-lookup"><span data-stu-id="e056a-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="e056a-107">En IotHub kan inte övergå mellan kostnads fria och betalda SKU: er och vice versa.</span><span class="sxs-lookup"><span data-stu-id="e056a-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="e056a-108">Du måste ta bort och återskapa iothub om du vill uppnå detta.</span><span class="sxs-lookup"><span data-stu-id="e056a-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="e056a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e056a-109">EXAMPLES</span></span>

### <span data-ttu-id="e056a-110">Exempel 1 skaffa giltiga SKU: er</span><span class="sxs-lookup"><span data-stu-id="e056a-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e056a-111">Hämtar en lista över alla SKU: er för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e056a-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e056a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e056a-112">PARAMETERS</span></span>

### <span data-ttu-id="e056a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e056a-113">-DefaultProfile</span></span>
<span data-ttu-id="e056a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e056a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e056a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e056a-115">-Name</span></span>
<span data-ttu-id="e056a-116">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="e056a-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="e056a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e056a-117">-ResourceGroupName</span></span>
<span data-ttu-id="e056a-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e056a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e056a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e056a-119">CommonParameters</span></span>
<span data-ttu-id="e056a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e056a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e056a-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e056a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e056a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e056a-122">INPUTS</span></span>

### <span data-ttu-id="e056a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e056a-123">System.String</span></span>

## <span data-ttu-id="e056a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e056a-124">OUTPUTS</span></span>

### <span data-ttu-id="e056a-125">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="e056a-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="e056a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e056a-126">NOTES</span></span>

## <span data-ttu-id="e056a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e056a-127">RELATED LINKS</span></span>
