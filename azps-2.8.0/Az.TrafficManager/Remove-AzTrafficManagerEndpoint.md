---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 60ce16c9c9933d326013ce03b74637b0fce4a3b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920930"
---
# <span data-ttu-id="71acc-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="71acc-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="71acc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71acc-102">SYNOPSIS</span></span>
<span data-ttu-id="71acc-103">Tar bort en slut punkt från Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="71acc-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="71acc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71acc-104">SYNTAX</span></span>

### <span data-ttu-id="71acc-105">Fält</span><span class="sxs-lookup"><span data-stu-id="71acc-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71acc-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="71acc-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71acc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71acc-107">DESCRIPTION</span></span>
<span data-ttu-id="71acc-108">Cmdleten **Remove-AzTrafficManagerEndpoint** tar bort en slut punkt från Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="71acc-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="71acc-109">Denna cmdlet aktiverar varje ändring i Traffic Manager-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="71acc-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="71acc-110">Om du vill ta bort flera slut punkter från ett lokalt Traffic Manager-Profile-objekt och genomföra ändringar i en enskild åtgärd använder du Remove-AzTrafficManagerEndpointConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71acc-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="71acc-111">Du kan använda pipeline-operatorn för att skicka ett **TrafficManagerEndpoint** -objekt till denna cmdlet, eller så kan du ange ett **TrafficManagerEndpoint** -objekt med hjälp av parametern *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="71acc-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="71acc-112">Alternativt kan du ange slut punktens namn och typ genom att använda parametrarna *Name* och *Type* tillsammans med parametrarna *Profilnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="71acc-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="71acc-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71acc-113">EXAMPLES</span></span>

### <span data-ttu-id="71acc-114">Exempel 1: ta bort en slut punkt från en profil</span><span class="sxs-lookup"><span data-stu-id="71acc-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="71acc-115">Det här kommandot tar bort Azure-slutpunkten med namnet contoso från den profil som heter ContosoProfile i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="71acc-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="71acc-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71acc-116">PARAMETERS</span></span>

### <span data-ttu-id="71acc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71acc-117">-DefaultProfile</span></span>
<span data-ttu-id="71acc-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71acc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71acc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="71acc-119">-Force</span></span>
<span data-ttu-id="71acc-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="71acc-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71acc-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="71acc-121">-Name</span></span>
<span data-ttu-id="71acc-122">Anger namnet på den trafik hanterarens slut punkt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="71acc-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71acc-123">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="71acc-123">-ProfileName</span></span>
<span data-ttu-id="71acc-124">Anger namnet på en Traffic Manager-profil som den här cmdleten tar bort en slut punkt för.</span><span class="sxs-lookup"><span data-stu-id="71acc-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="71acc-125">Använd Get-AzTrafficManagerProfile cmdlet för att få en profil.</span><span class="sxs-lookup"><span data-stu-id="71acc-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71acc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71acc-126">-ResourceGroupName</span></span>
<span data-ttu-id="71acc-127">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="71acc-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="71acc-128">Denna cmdlet tar bort en Traffic Manager-slutpunkt från en Traffic Manager-profil i den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="71acc-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71acc-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="71acc-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="71acc-130">Anger den trafik hanterarens slut punkt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="71acc-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="71acc-131">För att hämta ett **TrafficManagerEndpoint** -objekt, Använd cmdleten Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="71acc-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71acc-132">– Skriv</span><span class="sxs-lookup"><span data-stu-id="71acc-132">-Type</span></span>
<span data-ttu-id="71acc-133">Anger den typ av slut punkt som denna cmdlet lägger till i Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="71acc-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="71acc-134">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="71acc-134">Valid values are:</span></span> 

- <span data-ttu-id="71acc-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="71acc-135">AzureEndpoints</span></span>
- <span data-ttu-id="71acc-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="71acc-136">ExternalEndpoints</span></span>
- <span data-ttu-id="71acc-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="71acc-137">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71acc-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="71acc-138">-Confirm</span></span>
<span data-ttu-id="71acc-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71acc-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71acc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71acc-140">-WhatIf</span></span>
<span data-ttu-id="71acc-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="71acc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71acc-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="71acc-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71acc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71acc-143">CommonParameters</span></span>
<span data-ttu-id="71acc-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71acc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71acc-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71acc-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71acc-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71acc-146">INPUTS</span></span>

### <span data-ttu-id="71acc-147">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="71acc-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="71acc-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71acc-148">OUTPUTS</span></span>

### <span data-ttu-id="71acc-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71acc-149">System.Boolean</span></span>

## <span data-ttu-id="71acc-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71acc-150">NOTES</span></span>

## <span data-ttu-id="71acc-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71acc-151">RELATED LINKS</span></span>

[<span data-ttu-id="71acc-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="71acc-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="71acc-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="71acc-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="71acc-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="71acc-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="71acc-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="71acc-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="71acc-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="71acc-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


