---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 2cececec0610b813bf59a1ef8adac59e1fa8ddb2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258432"
---
# <span data-ttu-id="a78cc-101">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="a78cc-101">Add-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="a78cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a78cc-102">SYNOPSIS</span></span>
<span data-ttu-id="a78cc-103">Lägger till ett adress intervall eller ett undernät i ett lokalt Traffic Manager-slutobjekt.</span><span class="sxs-lookup"><span data-stu-id="a78cc-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="a78cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a78cc-104">SYNTAX</span></span>

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a78cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a78cc-105">DESCRIPTION</span></span>
<span data-ttu-id="a78cc-106">Cmdleten **Add-AzTrafficManagerIpAddressRange** lägger till ett IP-adressintervall till ett lokalt objekt i Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="a78cc-106">The **Add-AzTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="a78cc-107">Du kan få en slut punkt genom att använda New-AzTrafficManagerEndpoint eller Get-AzTrafficManagerEndpoint cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a78cc-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="a78cc-108">Denna cmdlet fungerar med det lokala slutpunktsmapparen.</span><span class="sxs-lookup"><span data-stu-id="a78cc-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="a78cc-109">Bekräfta dina ändringar av slut punkten för Traffic Manager genom att använda Set-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a78cc-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="a78cc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a78cc-110">EXAMPLES</span></span>

### <span data-ttu-id="a78cc-111">Exempel 1: lägga till IP-adressintervall i en slut punkt</span><span class="sxs-lookup"><span data-stu-id="a78cc-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="a78cc-112">Det första kommandot skapar en slut punkt för Azure Traffic Manager genom att använda cmdlet **New-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="a78cc-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="a78cc-113">Kommandot lagrar den lokala slut punkten i $TrafficManagerEndpoint variabel.</span><span class="sxs-lookup"><span data-stu-id="a78cc-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="a78cc-114">Det andra kommandot lägger till IP-adressintervallet 1.2.3.4 för att 5.6.7.8 till slut punkten som lagras i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a78cc-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="a78cc-115">Det tredje kommandot lägger till IP-adressintervallet 9.10.11.0 till 9.10.11.255 slut punkten som lagras i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a78cc-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="a78cc-116">Det fjärde kommandot verifierar att scopet matchar storleken på intervallet och lägger till IP-adressintervallet 12.13.14.0 till 12.13.14.31 till slut punkten som lagras i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a78cc-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="a78cc-117">Det femte kommandot lägger till IP-adressintervallet 15.16.17.18 till 15.16.17.18 slut punkten som lagras i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a78cc-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="a78cc-118">Kommandot uppdaterar slut punkten i Traffic Manager för att matcha det lokala värdet i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a78cc-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="a78cc-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a78cc-119">PARAMETERS</span></span>

### <span data-ttu-id="a78cc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a78cc-120">-DefaultProfile</span></span>
<span data-ttu-id="a78cc-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a78cc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a78cc-122">-Senaste</span><span class="sxs-lookup"><span data-stu-id="a78cc-122">-Last</span></span>
<span data-ttu-id="a78cc-123">Anger den sista IP-adressen i intervallet som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="a78cc-123">Specifies the last IP address in the range to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78cc-124">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="a78cc-124">-Scope</span></span>
<span data-ttu-id="a78cc-125">Anger omfattningen för det IP-adressintervall som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="a78cc-125">Specifies the scope of the IP address range to be added.</span></span>

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

### <span data-ttu-id="a78cc-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a78cc-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="a78cc-127">Anger ett lokalt **TrafficManagerEndpoint** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a78cc-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="a78cc-128">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="a78cc-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="a78cc-129">Du kan hämta ett **TrafficManagerEndpoint** -objekt med hjälp av Get-AzTrafficManagerEndpoint eller New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a78cc-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="a78cc-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a78cc-130">-Confirm</span></span>
<span data-ttu-id="a78cc-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a78cc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a78cc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a78cc-132">-WhatIf</span></span>
<span data-ttu-id="a78cc-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a78cc-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a78cc-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a78cc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a78cc-135">-Först</span><span class="sxs-lookup"><span data-stu-id="a78cc-135">-First</span></span>
<span data-ttu-id="a78cc-136">Anger den första IP-adressen i intervallet som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="a78cc-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="a78cc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a78cc-137">CommonParameters</span></span>
<span data-ttu-id="a78cc-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a78cc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a78cc-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a78cc-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a78cc-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a78cc-140">INPUTS</span></span>

### <span data-ttu-id="a78cc-141">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a78cc-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a78cc-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a78cc-142">OUTPUTS</span></span>

### <span data-ttu-id="a78cc-143">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a78cc-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a78cc-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a78cc-144">NOTES</span></span>

## <span data-ttu-id="a78cc-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a78cc-145">RELATED LINKS</span></span>

[<span data-ttu-id="a78cc-146">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="a78cc-146">Remove-AzTrafficManagerIpAddressRange</span></span>](./Remove-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="a78cc-147">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a78cc-147">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a78cc-148">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a78cc-148">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a78cc-149">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a78cc-149">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
