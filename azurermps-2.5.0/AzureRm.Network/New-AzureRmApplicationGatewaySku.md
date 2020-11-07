---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: cda4281b1bf52b9f0b94926bc66590d1bd741c44
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929349"
---
# <span data-ttu-id="ba1f6-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ba1f6-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="ba1f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba1f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ba1f6-103">Skapar en SKU för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ba1f6-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba1f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba1f6-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba1f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba1f6-105">DESCRIPTION</span></span>
<span data-ttu-id="ba1f6-106">Cmdleten **New-AzureRmApplicationGatewaySku** skapar en enhet för lagerhållning (SKU) för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ba1f6-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="ba1f6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba1f6-107">EXAMPLES</span></span>

### <span data-ttu-id="ba1f6-108">Exempel 1: skapa en SKU för en Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ba1f6-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="ba1f6-109">Det här kommandot skapar en SKU med namnet Standard_Small för en Azure Application Gateway och lagrar resultatet i variabeln som heter $SKU.</span><span class="sxs-lookup"><span data-stu-id="ba1f6-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="ba1f6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba1f6-110">PARAMETERS</span></span>

### <span data-ttu-id="ba1f6-111">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="ba1f6-111">-Capacity</span></span>
<span data-ttu-id="ba1f6-112">Anger antalet instanser av en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ba1f6-112">Specifies the number of instances of an application gateway.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba1f6-113">-DefaultProfile</span></span>
<span data-ttu-id="ba1f6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ba1f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba1f6-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ba1f6-115">-Name</span></span>
<span data-ttu-id="ba1f6-116">Anger namnet på SKU: n.</span><span class="sxs-lookup"><span data-stu-id="ba1f6-116">Specifies the name of the SKU.</span></span>

<span data-ttu-id="ba1f6-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ba1f6-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba1f6-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="ba1f6-118">Standard_Small</span></span>
- <span data-ttu-id="ba1f6-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="ba1f6-119">Standard_Medium</span></span>
- <span data-ttu-id="ba1f6-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="ba1f6-120">Standard_Large</span></span>
- <span data-ttu-id="ba1f6-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="ba1f6-121">WAF_Medium</span></span>
- <span data-ttu-id="ba1f6-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="ba1f6-122">WAF_Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1f6-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="ba1f6-123">-Tier</span></span>
<span data-ttu-id="ba1f6-124">Anger nivån för SKU.</span><span class="sxs-lookup"><span data-stu-id="ba1f6-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="ba1f6-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ba1f6-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba1f6-126">Standar</span><span class="sxs-lookup"><span data-stu-id="ba1f6-126">Standard</span></span>
- <span data-ttu-id="ba1f6-127">WAF</span><span class="sxs-lookup"><span data-stu-id="ba1f6-127">WAF</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1f6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba1f6-128">CommonParameters</span></span>
<span data-ttu-id="ba1f6-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba1f6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba1f6-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba1f6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba1f6-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba1f6-131">INPUTS</span></span>

### <span data-ttu-id="ba1f6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ba1f6-132">System.String</span></span>

## <span data-ttu-id="ba1f6-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba1f6-133">OUTPUTS</span></span>

### <span data-ttu-id="ba1f6-134">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ba1f6-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="ba1f6-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba1f6-135">NOTES</span></span>

## <span data-ttu-id="ba1f6-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba1f6-136">RELATED LINKS</span></span>

[<span data-ttu-id="ba1f6-137">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ba1f6-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="ba1f6-138">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ba1f6-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


