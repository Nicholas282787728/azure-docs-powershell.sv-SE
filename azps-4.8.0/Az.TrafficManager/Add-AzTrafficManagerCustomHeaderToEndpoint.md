---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 9a1be7c45c507746ae3b8c97f883a61de0da78db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259749"
---
# <span data-ttu-id="83cc1-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="83cc1-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="83cc1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="83cc1-103">Lägger till anpassad rubrik information i ett lokalt Traffic Manager-slutobjekt.</span><span class="sxs-lookup"><span data-stu-id="83cc1-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="83cc1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83cc1-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83cc1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83cc1-105">DESCRIPTION</span></span>
<span data-ttu-id="83cc1-106">Cmdleten **Add-AzTrafficManagerCustomHeaderToEndpoint** lägger till anpassad huvud information i ett lokalt objekt i Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="83cc1-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="83cc1-107">Du kan få en slut punkt genom att använda New-AzTrafficManagerEndpoint eller Get-AzTrafficManagerEndpoint cmdletar.</span><span class="sxs-lookup"><span data-stu-id="83cc1-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="83cc1-108">Denna cmdlet fungerar med det lokala slutpunktsmapparen.</span><span class="sxs-lookup"><span data-stu-id="83cc1-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="83cc1-109">Bekräfta dina ändringar av slut punkten för Traffic Manager genom att använda Set-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83cc1-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="83cc1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83cc1-110">EXAMPLES</span></span>

### <span data-ttu-id="83cc1-111">Exempel 1: lägga till anpassad rubrik information i en slut punkt</span><span class="sxs-lookup"><span data-stu-id="83cc1-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="83cc1-112">Det första kommandot skapar en slut punkt för Azure Traffic Manager genom att använda cmdlet **New-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="83cc1-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="83cc1-113">Kommandot lagrar den lokala slut punkten i $TrafficManagerEndpoint variabel.</span><span class="sxs-lookup"><span data-stu-id="83cc1-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="83cc1-114">Det andra kommandot lägger till anpassad huvud information till slut punkten som lagras i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="83cc1-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="83cc1-115">Kommandot uppdaterar slut punkten i Traffic Manager för att matcha det lokala värdet i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="83cc1-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="83cc1-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83cc1-116">PARAMETERS</span></span>

### <span data-ttu-id="83cc1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83cc1-117">-DefaultProfile</span></span>
<span data-ttu-id="83cc1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83cc1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83cc1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="83cc1-119">-Name</span></span>
<span data-ttu-id="83cc1-120">Anger namnet på den anpassade rubrik informationen som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="83cc1-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="83cc1-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="83cc1-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="83cc1-122">Anger ett lokalt **TrafficManagerEndpoint** -objekt.</span><span class="sxs-lookup"><span data-stu-id="83cc1-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="83cc1-123">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="83cc1-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="83cc1-124">Du kan hämta ett **TrafficManagerEndpoint** -objekt med hjälp av Get-AzTrafficManagerEndpoint eller New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83cc1-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="83cc1-125">-Värde</span><span class="sxs-lookup"><span data-stu-id="83cc1-125">-Value</span></span>
<span data-ttu-id="83cc1-126">Anger värdet på den anpassade huvud rubrik informationen som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="83cc1-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="83cc1-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="83cc1-127">-Confirm</span></span>
<span data-ttu-id="83cc1-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83cc1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83cc1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83cc1-129">-WhatIf</span></span>
<span data-ttu-id="83cc1-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="83cc1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83cc1-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="83cc1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83cc1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83cc1-132">CommonParameters</span></span>
<span data-ttu-id="83cc1-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83cc1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83cc1-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83cc1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83cc1-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83cc1-135">INPUTS</span></span>

### <span data-ttu-id="83cc1-136">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="83cc1-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="83cc1-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83cc1-137">OUTPUTS</span></span>

### <span data-ttu-id="83cc1-138">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="83cc1-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="83cc1-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83cc1-139">NOTES</span></span>

## <span data-ttu-id="83cc1-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83cc1-140">RELATED LINKS</span></span>

[<span data-ttu-id="83cc1-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="83cc1-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="83cc1-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="83cc1-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="83cc1-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="83cc1-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="83cc1-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="83cc1-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)