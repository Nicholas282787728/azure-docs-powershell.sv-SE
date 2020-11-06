---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 8856a2f9f1a65d6d312571d75e2400a7dcf30bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580496"
---
# <span data-ttu-id="96d69-101">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d69-101">Set-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="96d69-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96d69-102">SYNOPSIS</span></span>
<span data-ttu-id="96d69-103">Uppdaterar en hanterings slut punkt för trafik.</span><span class="sxs-lookup"><span data-stu-id="96d69-103">Updates a Traffic Manager endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96d69-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96d69-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96d69-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96d69-105">DESCRIPTION</span></span>
<span data-ttu-id="96d69-106">Cmdleten **set-AzureRmTrafficManagerEndpoint** uppdaterar en slut punkt i Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="96d69-106">The **Set-AzureRmTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="96d69-107">Denna cmdlet uppdaterar inställningarna från ett lokalt slut punkts objekt.</span><span class="sxs-lookup"><span data-stu-id="96d69-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="96d69-108">Du kan ange ett slut punkts objekt genom att använda parametern *TrafficManagerEndpoint* eller genom att använda pipeline.</span><span class="sxs-lookup"><span data-stu-id="96d69-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="96d69-109">Du kan hämta ett lokalt objekt som representerar en slut punkt med hjälp av Get-AzureRmTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96d69-109">You can obtain a local object that represents an endpoint by using the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="96d69-110">Ändra objektet lokalt och Använd sedan **set-AzureRmTrafficManagerEndpoint** för att bekräfta dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="96d69-110">Modify the object locally and then use **Set-AzureRmTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="96d69-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96d69-111">EXAMPLES</span></span>

### <span data-ttu-id="96d69-112">Exempel 1: uppdatera en slut punkt</span><span class="sxs-lookup"><span data-stu-id="96d69-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="96d69-113">Det första kommandot får en slut punkt för Azure Traffic Manager genom att använda cmdleten **Get-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="96d69-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="96d69-114">Kommandot lagrar slut punkten lokalt i $TrafficManagerEndpoint variabel.</span><span class="sxs-lookup"><span data-stu-id="96d69-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="96d69-115">Det andra kommandot ändrar slut punkten lokalt.</span><span class="sxs-lookup"><span data-stu-id="96d69-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="96d69-116">Det här kommandot ändrar slut punkts vikten till 20.</span><span class="sxs-lookup"><span data-stu-id="96d69-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="96d69-117">Det tredje kommandot uppdaterar slut punkten i Traffic Manager för att matcha det lokala värdet i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="96d69-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="96d69-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96d69-118">PARAMETERS</span></span>

### <span data-ttu-id="96d69-119">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d69-119">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="96d69-120">Anger ett lokalt **TrafficManagerEndpoint** -objekt.</span><span class="sxs-lookup"><span data-stu-id="96d69-120">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="96d69-121">Denna cmdlet uppdaterar trafik hanteraren så att den matchar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="96d69-121">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96d69-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d69-122">-DefaultProfile</span></span>
<span data-ttu-id="96d69-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96d69-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96d69-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d69-124">CommonParameters</span></span>
<span data-ttu-id="96d69-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96d69-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d69-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96d69-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d69-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96d69-127">INPUTS</span></span>

### <span data-ttu-id="96d69-128">Microsoft. Azure. commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d69-128">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="96d69-129">Denna cmdlet accepterar ett **TrafficManagerEndpoint** -objekt.</span><span class="sxs-lookup"><span data-stu-id="96d69-129">This cmdlet accepts a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="96d69-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96d69-130">OUTPUTS</span></span>

### <span data-ttu-id="96d69-131">Microsoft. Azure. commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d69-131">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="96d69-132">Denna cmdlet returnerar ett **TrafficManagerEndpoint** -objekt.</span><span class="sxs-lookup"><span data-stu-id="96d69-132">This cmdlet returns a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="96d69-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96d69-133">NOTES</span></span>

## <span data-ttu-id="96d69-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96d69-134">RELATED LINKS</span></span>

