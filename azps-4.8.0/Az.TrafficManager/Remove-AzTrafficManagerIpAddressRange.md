---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: bfeef76b700eb408da89561464bc5457f94cdd4a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260871"
---
# <span data-ttu-id="f331d-101">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="f331d-101">Remove-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="f331d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f331d-102">SYNOPSIS</span></span>
<span data-ttu-id="f331d-103">Tar bort ett adress intervall eller ett undernät från ett lokalt Traffic Manager-slutobjekt.</span><span class="sxs-lookup"><span data-stu-id="f331d-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="f331d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f331d-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f331d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f331d-105">DESCRIPTION</span></span>
<span data-ttu-id="f331d-106">Cmdleten **Remove-AzTrafficManagerIpAddressRange** tar bort ett IP-adressintervall från ett lokalt objekt i Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="f331d-106">The **Remove-AzTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="f331d-107">Du kan få en slut punkt genom att använda New-AzTrafficManagerEndpoint eller Get-AzTrafficManagerEndpoint cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f331d-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="f331d-108">Denna cmdlet fungerar med det lokala slutpunktsmapparen.</span><span class="sxs-lookup"><span data-stu-id="f331d-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="f331d-109">Bekräfta dina ändringar av slut punkten för Traffic Manager genom att använda Set-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f331d-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="f331d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f331d-110">EXAMPLES</span></span>

### <span data-ttu-id="f331d-111">Exempel 1: ta bort IP-adressintervall från en slut punkt</span><span class="sxs-lookup"><span data-stu-id="f331d-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="f331d-112">Det första kommandot får Azure-slutpunkten contoso från den profil som heter ContosoProfile i resurs gruppen med namnet ResourceGroup11 och lagrar sedan objektet i $TrafficManagerEndpoint variabel.</span><span class="sxs-lookup"><span data-stu-id="f331d-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="f331d-113">Det andra kommandot tar bort ett IP-adressintervall från slut punkten som lagras i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f331d-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="f331d-114">Kommandot uppdaterar slut punkten i Traffic Manager för att matcha det lokala värdet i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f331d-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="f331d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f331d-115">PARAMETERS</span></span>

### <span data-ttu-id="f331d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f331d-116">-DefaultProfile</span></span>
<span data-ttu-id="f331d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f331d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f331d-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f331d-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="f331d-119">Anger ett lokalt **TrafficManagerEndpoint** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f331d-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="f331d-120">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="f331d-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="f331d-121">Du kan hämta ett **TrafficManagerEndpoint** -objekt med hjälp av Get-AzTrafficManagerEndpoint eller New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f331d-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="f331d-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f331d-122">-Confirm</span></span>
<span data-ttu-id="f331d-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f331d-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f331d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f331d-124">-WhatIf</span></span>
<span data-ttu-id="f331d-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f331d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f331d-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f331d-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f331d-127">-Först</span><span class="sxs-lookup"><span data-stu-id="f331d-127">-First</span></span>
<span data-ttu-id="f331d-128">Anger den första IP-adressen i det område som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f331d-128">Specifies the first IP address in the range to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f331d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f331d-129">CommonParameters</span></span>
<span data-ttu-id="f331d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f331d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f331d-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f331d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f331d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f331d-132">INPUTS</span></span>

### <span data-ttu-id="f331d-133">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f331d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="f331d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f331d-134">OUTPUTS</span></span>

### <span data-ttu-id="f331d-135">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f331d-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="f331d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f331d-136">NOTES</span></span>

## <span data-ttu-id="f331d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f331d-137">RELATED LINKS</span></span>

[<span data-ttu-id="f331d-138">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="f331d-138">Add-AzTrafficManagerIpAddressRange</span></span>](./Add-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="f331d-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f331d-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="f331d-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f331d-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="f331d-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f331d-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
