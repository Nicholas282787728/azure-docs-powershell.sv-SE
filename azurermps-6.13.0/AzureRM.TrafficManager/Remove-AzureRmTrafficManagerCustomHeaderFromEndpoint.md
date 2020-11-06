---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 452e252b7bf9368ea89e81f2d37fd5a80ab079b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573841"
---
# <span data-ttu-id="0194e-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="0194e-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="0194e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0194e-102">SYNOPSIS</span></span>
<span data-ttu-id="0194e-103">Tar bort anpassad huvud information från ett lokalt Traffic Manager-slutobjekt.</span><span class="sxs-lookup"><span data-stu-id="0194e-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0194e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0194e-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -Name <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0194e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0194e-105">DESCRIPTION</span></span>
<span data-ttu-id="0194e-106">Cmdleten **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** tar bort anpassad huvud information från ett lokalt objekt i Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="0194e-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="0194e-107">Du kan få en slut punkt genom att använda New-AzureRmTrafficManagerEndpoint eller Get-AzureRmTrafficManagerEndpoint cmdletar.</span><span class="sxs-lookup"><span data-stu-id="0194e-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="0194e-108">Denna cmdlet fungerar med det lokala slutpunktsmapparen.</span><span class="sxs-lookup"><span data-stu-id="0194e-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="0194e-109">Bekräfta dina ändringar av slut punkten för Traffic Manager genom att använda Set-AzureRmTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0194e-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="0194e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0194e-110">EXAMPLES</span></span>

### <span data-ttu-id="0194e-111">Exempel 1: ta bort anpassad under näts information från en slut punkt</span><span class="sxs-lookup"><span data-stu-id="0194e-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="0194e-112">Det första kommandot får Azure-slutpunkten contoso från den profil som heter ContosoProfile i resurs gruppen med namnet ResourceGroup11 och lagrar sedan objektet i $TrafficManagerEndpoint variabel.</span><span class="sxs-lookup"><span data-stu-id="0194e-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="0194e-113">Det andra kommandot tar bort den anpassade huvud rubrik informationen från slut punkten som lagras i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0194e-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="0194e-114">Kommandot uppdaterar slut punkten i Traffic Manager för att matcha det lokala värdet i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0194e-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="0194e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0194e-115">PARAMETERS</span></span>

### <span data-ttu-id="0194e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0194e-116">-DefaultProfile</span></span>
<span data-ttu-id="0194e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0194e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0194e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="0194e-118">-Name</span></span>
<span data-ttu-id="0194e-119">Anger namnet på den anpassade huvud informationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0194e-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="0194e-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0194e-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="0194e-121">Anger ett lokalt **TrafficManagerEndpoint** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0194e-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="0194e-122">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="0194e-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="0194e-123">Du kan hämta ett **TrafficManagerEndpoint** -objekt med hjälp av Get-AzureRmTrafficManagerEndpoint eller New-AzureRmTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0194e-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="0194e-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0194e-124">-Confirm</span></span>
<span data-ttu-id="0194e-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0194e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0194e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0194e-126">-WhatIf</span></span>
<span data-ttu-id="0194e-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0194e-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0194e-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0194e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0194e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0194e-129">CommonParameters</span></span>
<span data-ttu-id="0194e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0194e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0194e-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0194e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0194e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0194e-132">INPUTS</span></span>

### <span data-ttu-id="0194e-133">Microsoft. Azure. commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0194e-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="0194e-134">Denna cmdlet accepterar ett **TrafficManagerEndpoint** -objekt till denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0194e-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="0194e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0194e-135">OUTPUTS</span></span>

### <span data-ttu-id="0194e-136">Microsoft. Azure. commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0194e-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="0194e-137">Denna cmdlet returnerar ett ändrat TrafficManagerEndpoint-objekt.</span><span class="sxs-lookup"><span data-stu-id="0194e-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="0194e-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0194e-138">NOTES</span></span>

## <span data-ttu-id="0194e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0194e-139">RELATED LINKS</span></span>

[<span data-ttu-id="0194e-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="0194e-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="0194e-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0194e-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="0194e-142">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0194e-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="0194e-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0194e-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
