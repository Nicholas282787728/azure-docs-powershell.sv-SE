---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521890"
---
# <span data-ttu-id="476ae-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="476ae-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="476ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="476ae-102">SYNOPSIS</span></span>
<span data-ttu-id="476ae-103">Skapar en SKU för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="476ae-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="476ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="476ae-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="476ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="476ae-105">DESCRIPTION</span></span>
<span data-ttu-id="476ae-106">Cmdleten **New-AzApplicationGatewaySku** skapar en enhet för lagerhållning (SKU) för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="476ae-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="476ae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="476ae-107">EXAMPLES</span></span>

### <span data-ttu-id="476ae-108">Exempel 1: skapa en SKU för en Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="476ae-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="476ae-109">Det här kommandot skapar en SKU med namnet Standard_Small för en Azure Application Gateway och lagrar resultatet i variabeln som heter $SKU.</span><span class="sxs-lookup"><span data-stu-id="476ae-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="476ae-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="476ae-110">PARAMETERS</span></span>

### <span data-ttu-id="476ae-111">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="476ae-111">-Capacity</span></span>
<span data-ttu-id="476ae-112">Anger antalet instanser av en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="476ae-112">Specifies the number of instances of an application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="476ae-113">-DefaultProfile</span></span>
<span data-ttu-id="476ae-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="476ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="476ae-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="476ae-115">-Name</span></span>
<span data-ttu-id="476ae-116">Anger namnet på SKU: n.</span><span class="sxs-lookup"><span data-stu-id="476ae-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="476ae-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="476ae-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="476ae-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="476ae-118">Standard_Small</span></span>
- <span data-ttu-id="476ae-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="476ae-119">Standard_Medium</span></span>
- <span data-ttu-id="476ae-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="476ae-120">Standard_Large</span></span>
- <span data-ttu-id="476ae-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="476ae-121">WAF_Medium</span></span>
- <span data-ttu-id="476ae-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="476ae-122">WAF_Large</span></span>
- <span data-ttu-id="476ae-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="476ae-123">Standard_v2</span></span>
- <span data-ttu-id="476ae-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="476ae-124">WAF_v2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476ae-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="476ae-125">-Tier</span></span>
<span data-ttu-id="476ae-126">Anger nivån för SKU.</span><span class="sxs-lookup"><span data-stu-id="476ae-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="476ae-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="476ae-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="476ae-128">Standar</span><span class="sxs-lookup"><span data-stu-id="476ae-128">Standard</span></span>
- <span data-ttu-id="476ae-129">WAF</span><span class="sxs-lookup"><span data-stu-id="476ae-129">WAF</span></span>
- <span data-ttu-id="476ae-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="476ae-130">Standard_v2</span></span>
- <span data-ttu-id="476ae-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="476ae-131">WAF_v2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, WAF, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476ae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476ae-132">CommonParameters</span></span>
<span data-ttu-id="476ae-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="476ae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476ae-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="476ae-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476ae-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="476ae-135">INPUTS</span></span>

### <span data-ttu-id="476ae-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="476ae-136">None</span></span>

## <span data-ttu-id="476ae-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="476ae-137">OUTPUTS</span></span>

### <span data-ttu-id="476ae-138">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="476ae-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="476ae-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="476ae-139">NOTES</span></span>

## <span data-ttu-id="476ae-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="476ae-140">RELATED LINKS</span></span>

[<span data-ttu-id="476ae-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="476ae-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="476ae-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="476ae-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


