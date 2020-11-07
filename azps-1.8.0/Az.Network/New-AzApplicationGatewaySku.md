---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 1d737733deb167510196555af4ad7b357cc60154
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748105"
---
# <span data-ttu-id="d6ea4-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d6ea4-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="d6ea4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ea4-103">Skapar en SKU för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="d6ea4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6ea4-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6ea4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6ea4-105">DESCRIPTION</span></span>
<span data-ttu-id="d6ea4-106">Cmdleten **New-AzApplicationGatewaySku** skapar en enhet för lagerhållning (SKU) för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="d6ea4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6ea4-107">EXAMPLES</span></span>

### <span data-ttu-id="d6ea4-108">Exempel 1: skapa en SKU för en Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d6ea4-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="d6ea4-109">Det här kommandot skapar en SKU med namnet Standard_Small för en Azure Application Gateway och lagrar resultatet i variabeln som heter $SKU.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="d6ea4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6ea4-110">PARAMETERS</span></span>

### <span data-ttu-id="d6ea4-111">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="d6ea4-111">-Capacity</span></span>
<span data-ttu-id="d6ea4-112">Anger antalet instanser av en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="d6ea4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ea4-113">-DefaultProfile</span></span>
<span data-ttu-id="d6ea4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6ea4-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6ea4-115">-Name</span></span>
<span data-ttu-id="d6ea4-116">Anger namnet på SKU: n.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="d6ea4-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d6ea4-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6ea4-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="d6ea4-118">Standard_Small</span></span>
- <span data-ttu-id="d6ea4-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="d6ea4-119">Standard_Medium</span></span>
- <span data-ttu-id="d6ea4-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="d6ea4-120">Standard_Large</span></span>
- <span data-ttu-id="d6ea4-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="d6ea4-121">WAF_Medium</span></span>
- <span data-ttu-id="d6ea4-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="d6ea4-122">WAF_Large</span></span>

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

### <span data-ttu-id="d6ea4-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="d6ea4-123">-Tier</span></span>
<span data-ttu-id="d6ea4-124">Anger nivån för SKU.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="d6ea4-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d6ea4-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6ea4-126">Standar</span><span class="sxs-lookup"><span data-stu-id="d6ea4-126">Standard</span></span>
- <span data-ttu-id="d6ea4-127">WAF</span><span class="sxs-lookup"><span data-stu-id="d6ea4-127">WAF</span></span>

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

### <span data-ttu-id="d6ea4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ea4-128">CommonParameters</span></span>
<span data-ttu-id="d6ea4-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ea4-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6ea4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ea4-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6ea4-131">INPUTS</span></span>

### <span data-ttu-id="d6ea4-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="d6ea4-132">None</span></span>

## <span data-ttu-id="d6ea4-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6ea4-133">OUTPUTS</span></span>

### <span data-ttu-id="d6ea4-134">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d6ea4-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="d6ea4-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6ea4-135">NOTES</span></span>

## <span data-ttu-id="d6ea4-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6ea4-136">RELATED LINKS</span></span>

[<span data-ttu-id="d6ea4-137">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d6ea4-137">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="d6ea4-138">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d6ea4-138">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


