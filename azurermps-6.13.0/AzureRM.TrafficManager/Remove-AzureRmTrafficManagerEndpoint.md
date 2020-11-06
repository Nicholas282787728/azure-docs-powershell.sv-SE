---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: da42677edbb9083df3c9a5a11b4d4910eda7dc84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583380"
---
# <span data-ttu-id="9587b-101">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9587b-101">Remove-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="9587b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9587b-102">SYNOPSIS</span></span>
<span data-ttu-id="9587b-103">Tar bort en slut punkt från Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="9587b-103">Removes an endpoint from Traffic Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9587b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9587b-104">SYNTAX</span></span>

### <span data-ttu-id="9587b-105">Fält</span><span class="sxs-lookup"><span data-stu-id="9587b-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9587b-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="9587b-106">Object</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9587b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9587b-107">DESCRIPTION</span></span>
<span data-ttu-id="9587b-108">Cmdleten **Remove-AzureRmTrafficManagerEndpoint** tar bort en slut punkt från Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="9587b-108">The **Remove-AzureRmTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="9587b-109">Denna cmdlet aktiverar varje ändring i Traffic Manager-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9587b-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="9587b-110">Om du vill ta bort flera slut punkter från ett lokalt Traffic Manager-Profile-objekt och genomföra ändringar i en enskild åtgärd använder du Remove-AzureRmTrafficManagerEndpointConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9587b-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="9587b-111">Du kan använda pipeline-operatorn för att skicka ett **TrafficManagerEndpoint** -objekt till denna cmdlet, eller så kan du ange ett **TrafficManagerEndpoint** -objekt med hjälp av parametern *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="9587b-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="9587b-112">Alternativt kan du ange slut punktens namn och typ genom att använda parametrarna *Name* och *Type* tillsammans med parametrarna *Profilnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="9587b-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="9587b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9587b-113">EXAMPLES</span></span>

### <span data-ttu-id="9587b-114">Exempel 1: ta bort en slut punkt från en profil</span><span class="sxs-lookup"><span data-stu-id="9587b-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="9587b-115">Det här kommandot tar bort Azure-slutpunkten med namnet contoso från den profil som heter ContosoProfile i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9587b-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="9587b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9587b-116">PARAMETERS</span></span>

### <span data-ttu-id="9587b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9587b-117">-DefaultProfile</span></span>
<span data-ttu-id="9587b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9587b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9587b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9587b-119">-Force</span></span>
<span data-ttu-id="9587b-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9587b-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9587b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9587b-121">-Name</span></span>
<span data-ttu-id="9587b-122">Anger namnet på den trafik hanterarens slut punkt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="9587b-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9587b-123">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="9587b-123">-ProfileName</span></span>
<span data-ttu-id="9587b-124">Anger namnet på en Traffic Manager-profil som den här cmdleten tar bort en slut punkt för.</span><span class="sxs-lookup"><span data-stu-id="9587b-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="9587b-125">Använd Get-AzureRmTrafficManagerProfile cmdlet för att få en profil.</span><span class="sxs-lookup"><span data-stu-id="9587b-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="9587b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9587b-126">-ResourceGroupName</span></span>
<span data-ttu-id="9587b-127">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9587b-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9587b-128">Denna cmdlet tar bort en Traffic Manager-slutpunkt från en Traffic Manager-profil i den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9587b-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9587b-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9587b-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="9587b-130">Anger den trafik hanterarens slut punkt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="9587b-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="9587b-131">För att hämta ett **TrafficManagerEndpoint** -objekt, Använd cmdleten Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9587b-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="9587b-132">– Skriv</span><span class="sxs-lookup"><span data-stu-id="9587b-132">-Type</span></span>
<span data-ttu-id="9587b-133">Anger den typ av slut punkt som denna cmdlet lägger till i Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="9587b-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="9587b-134">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="9587b-134">Valid values are:</span></span> 

- <span data-ttu-id="9587b-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="9587b-135">AzureEndpoints</span></span>
- <span data-ttu-id="9587b-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="9587b-136">ExternalEndpoints</span></span>
- <span data-ttu-id="9587b-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="9587b-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="9587b-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9587b-138">-Confirm</span></span>
<span data-ttu-id="9587b-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9587b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9587b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9587b-140">-WhatIf</span></span>
<span data-ttu-id="9587b-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9587b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9587b-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9587b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9587b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9587b-143">CommonParameters</span></span>
<span data-ttu-id="9587b-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9587b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9587b-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9587b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9587b-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9587b-146">INPUTS</span></span>

### <span data-ttu-id="9587b-147">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9587b-147">TrafficManagerEndpoint</span></span>
<span data-ttu-id="9587b-148">Parametern ' TrafficManagerEndpoint ' godkänner värdet av typen ' TrafficManagerEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9587b-148">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="9587b-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9587b-149">OUTPUTS</span></span>

### <span data-ttu-id="9587b-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9587b-150">System.Boolean</span></span>

## <span data-ttu-id="9587b-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9587b-151">NOTES</span></span>

## <span data-ttu-id="9587b-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9587b-152">RELATED LINKS</span></span>

[<span data-ttu-id="9587b-153">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9587b-153">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="9587b-154">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9587b-154">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9587b-155">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9587b-155">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="9587b-156">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="9587b-156">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="9587b-157">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9587b-157">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


