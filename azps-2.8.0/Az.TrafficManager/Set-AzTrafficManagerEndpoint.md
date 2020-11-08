---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 31201d607d1b9f0825236fe162bf86028b148193
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921120"
---
# <span data-ttu-id="ef2f6-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef2f6-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="ef2f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ef2f6-103">Uppdaterar en hanterings slut punkt för trafik.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="ef2f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef2f6-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef2f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef2f6-105">DESCRIPTION</span></span>
<span data-ttu-id="ef2f6-106">Cmdleten **set-AzTrafficManagerEndpoint** uppdaterar en slut punkt i Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="ef2f6-107">Denna cmdlet uppdaterar inställningarna från ett lokalt slut punkts objekt.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="ef2f6-108">Du kan ange ett slut punkts objekt genom att använda parametern *TrafficManagerEndpoint* eller genom att använda pipeline.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="ef2f6-109">Du kan hämta ett lokalt objekt som representerar en slut punkt med hjälp av Get-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="ef2f6-110">Ändra objektet lokalt och Använd sedan **set-AzTrafficManagerEndpoint** för att bekräfta dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="ef2f6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef2f6-111">EXAMPLES</span></span>

### <span data-ttu-id="ef2f6-112">Exempel 1: uppdatera en slut punkt</span><span class="sxs-lookup"><span data-stu-id="ef2f6-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="ef2f6-113">Det första kommandot får en slut punkt för Azure Traffic Manager genom att använda cmdleten **Get-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="ef2f6-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="ef2f6-114">Kommandot lagrar slut punkten lokalt i $TrafficManagerEndpoint variabel.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="ef2f6-115">Det andra kommandot ändrar slut punkten lokalt.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="ef2f6-116">Det här kommandot ändrar slut punkts vikten till 20.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="ef2f6-117">Det tredje kommandot uppdaterar slut punkten i Traffic Manager för att matcha det lokala värdet i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="ef2f6-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef2f6-118">PARAMETERS</span></span>

### <span data-ttu-id="ef2f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef2f6-119">-DefaultProfile</span></span>
<span data-ttu-id="ef2f6-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef2f6-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef2f6-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="ef2f6-122">Anger ett lokalt **TrafficManagerEndpoint** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="ef2f6-123">Denna cmdlet uppdaterar trafik hanteraren så att den matchar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="ef2f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef2f6-124">CommonParameters</span></span>
<span data-ttu-id="ef2f6-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef2f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef2f6-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef2f6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef2f6-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef2f6-127">INPUTS</span></span>

### <span data-ttu-id="ef2f6-128">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef2f6-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ef2f6-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef2f6-129">OUTPUTS</span></span>

### <span data-ttu-id="ef2f6-130">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef2f6-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ef2f6-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef2f6-131">NOTES</span></span>

## <span data-ttu-id="ef2f6-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef2f6-132">RELATED LINKS</span></span>