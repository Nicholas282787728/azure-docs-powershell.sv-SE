---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: eb1f0dadd905ff4b57a58c46f763f3c2dd51f256
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583236"
---
# <span data-ttu-id="1b771-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="1b771-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="1b771-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b771-102">SYNOPSIS</span></span>
<span data-ttu-id="1b771-103">Skapar en SKU för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="1b771-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b771-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b771-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b771-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b771-105">DESCRIPTION</span></span>
<span data-ttu-id="1b771-106">Cmdleten **New-AzureRmApplicationGatewaySku** skapar en enhet för lagerhållning (SKU) för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1b771-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="1b771-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b771-107">EXAMPLES</span></span>

### <span data-ttu-id="1b771-108">Exempel 1: skapa en SKU för en Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1b771-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="1b771-109">Det här kommandot skapar en SKU med namnet Standard_Small för en Azure Application Gateway och lagrar resultatet i variabeln som heter $SKU.</span><span class="sxs-lookup"><span data-stu-id="1b771-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="1b771-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b771-110">PARAMETERS</span></span>

### <span data-ttu-id="1b771-111">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="1b771-111">-Capacity</span></span>
<span data-ttu-id="1b771-112">Anger antalet instanser av en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="1b771-112">Specifies the number of instances of an application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b771-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b771-113">-Name</span></span>
<span data-ttu-id="1b771-114">Anger namnet på SKU: n.</span><span class="sxs-lookup"><span data-stu-id="1b771-114">Specifies the name of the SKU.</span></span>

<span data-ttu-id="1b771-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1b771-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1b771-116">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="1b771-116">Standard_Small</span></span>
- <span data-ttu-id="1b771-117">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="1b771-117">Standard_Medium</span></span>
- <span data-ttu-id="1b771-118">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="1b771-118">Standard_Large</span></span>
- <span data-ttu-id="1b771-119">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="1b771-119">WAF_Medium</span></span>
- <span data-ttu-id="1b771-120">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="1b771-120">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b771-121">-Tier</span><span class="sxs-lookup"><span data-stu-id="1b771-121">-Tier</span></span>
<span data-ttu-id="1b771-122">Anger nivån för SKU.</span><span class="sxs-lookup"><span data-stu-id="1b771-122">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="1b771-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1b771-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1b771-124">Standar</span><span class="sxs-lookup"><span data-stu-id="1b771-124">Standard</span></span>
- <span data-ttu-id="1b771-125">WAF</span><span class="sxs-lookup"><span data-stu-id="1b771-125">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b771-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b771-126">-DefaultProfile</span></span>
<span data-ttu-id="1b771-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b771-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b771-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b771-128">CommonParameters</span></span>
<span data-ttu-id="1b771-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b771-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b771-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b771-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b771-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b771-131">INPUTS</span></span>

### <span data-ttu-id="1b771-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1b771-132">System.String</span></span>

## <span data-ttu-id="1b771-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b771-133">OUTPUTS</span></span>

### <span data-ttu-id="1b771-134">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="1b771-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="1b771-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b771-135">NOTES</span></span>

## <span data-ttu-id="1b771-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b771-136">RELATED LINKS</span></span>

[<span data-ttu-id="1b771-137">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="1b771-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="1b771-138">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="1b771-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


