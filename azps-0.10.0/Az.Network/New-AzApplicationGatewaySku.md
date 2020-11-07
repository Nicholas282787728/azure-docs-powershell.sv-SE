---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 0b87119ccec521b85a210dc8685874bd4ba4b9ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922157"
---
# <span data-ttu-id="ac9c9-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ac9c9-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="ac9c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9c9-103">Skapar en SKU för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="ac9c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac9c9-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac9c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac9c9-105">DESCRIPTION</span></span>
<span data-ttu-id="ac9c9-106">Cmdleten **New-AzApplicationGatewaySku** skapar en enhet för lagerhållning (SKU) för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="ac9c9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac9c9-107">EXAMPLES</span></span>

### <span data-ttu-id="ac9c9-108">Exempel 1: skapa en SKU för en Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ac9c9-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="ac9c9-109">Det här kommandot skapar en SKU med namnet Standard_Small för en Azure Application Gateway och lagrar resultatet i variabeln som heter $SKU.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="ac9c9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac9c9-110">PARAMETERS</span></span>

### <span data-ttu-id="ac9c9-111">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="ac9c9-111">-Capacity</span></span>
<span data-ttu-id="ac9c9-112">Anger antalet instanser av en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="ac9c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9c9-113">-DefaultProfile</span></span>
<span data-ttu-id="ac9c9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac9c9-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac9c9-115">-Name</span></span>
<span data-ttu-id="ac9c9-116">Anger namnet på SKU: n.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-116">Specifies the name of the SKU.</span></span>

<span data-ttu-id="ac9c9-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ac9c9-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ac9c9-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="ac9c9-118">Standard_Small</span></span>
- <span data-ttu-id="ac9c9-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="ac9c9-119">Standard_Medium</span></span>
- <span data-ttu-id="ac9c9-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="ac9c9-120">Standard_Large</span></span>
- <span data-ttu-id="ac9c9-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="ac9c9-121">WAF_Medium</span></span>
- <span data-ttu-id="ac9c9-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="ac9c9-122">WAF_Large</span></span>

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

### <span data-ttu-id="ac9c9-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="ac9c9-123">-Tier</span></span>
<span data-ttu-id="ac9c9-124">Anger nivån för SKU.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="ac9c9-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ac9c9-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ac9c9-126">Standar</span><span class="sxs-lookup"><span data-stu-id="ac9c9-126">Standard</span></span>
- <span data-ttu-id="ac9c9-127">WAF</span><span class="sxs-lookup"><span data-stu-id="ac9c9-127">WAF</span></span>

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

### <span data-ttu-id="ac9c9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9c9-128">CommonParameters</span></span>
<span data-ttu-id="ac9c9-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac9c9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9c9-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9c9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9c9-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac9c9-131">INPUTS</span></span>

### <span data-ttu-id="ac9c9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ac9c9-132">System.String</span></span>

## <span data-ttu-id="ac9c9-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac9c9-133">OUTPUTS</span></span>

### <span data-ttu-id="ac9c9-134">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ac9c9-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="ac9c9-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac9c9-135">NOTES</span></span>

## <span data-ttu-id="ac9c9-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac9c9-136">RELATED LINKS</span></span>

[<span data-ttu-id="ac9c9-137">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ac9c9-137">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="ac9c9-138">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ac9c9-138">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


