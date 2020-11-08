---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 037a670c0e96d1a9014cd19b32a7d2ba4da282ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272508"
---
# <span data-ttu-id="15c6a-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15c6a-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="15c6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="15c6a-103">Inaktiverar en slut punkt i en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="15c6a-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="15c6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15c6a-104">SYNTAX</span></span>

### <span data-ttu-id="15c6a-105">Fält</span><span class="sxs-lookup"><span data-stu-id="15c6a-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15c6a-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="15c6a-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15c6a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15c6a-107">DESCRIPTION</span></span>
<span data-ttu-id="15c6a-108">Cmdleten **disable-AzTrafficManagerEndpoint** inaktiverar en slut punkt i en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="15c6a-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="15c6a-109">Du kan använda pipeline-operatorn för att skicka ett **TrafficManagerEndpoint** -objekt till denna cmdlet, eller så kan du skicka ett **TrafficManagerEndpoint** -objekt med parametern *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="15c6a-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="15c6a-110">Alternativt kan du ange slut punktens namn och typ genom att använda parametrarna *Name* och *Type* tillsammans med parametrarna *Profilnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="15c6a-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="15c6a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15c6a-111">EXAMPLES</span></span>

### <span data-ttu-id="15c6a-112">Exempel 1: inaktivera en slut punkt efter namn</span><span class="sxs-lookup"><span data-stu-id="15c6a-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="15c6a-113">Det här kommandot inaktiverar den externa slut punkten med namnet contoso i profilen med namnet ContosoProfile i resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="15c6a-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="15c6a-114">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="15c6a-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="15c6a-115">Exempel 2: inaktivera en slut punkt genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="15c6a-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="15c6a-116">Det här kommandot får den externa slut punkten namnet contoso från den profil som heter ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="15c6a-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="15c6a-117">Kommandot skickar sedan slut punkten till cmdleten **disable-AzTrafficManagerEndpoint** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="15c6a-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="15c6a-118">Denna cmdlet inaktiverar slut punkten.</span><span class="sxs-lookup"><span data-stu-id="15c6a-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="15c6a-119">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="15c6a-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="15c6a-120">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="15c6a-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="15c6a-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15c6a-121">PARAMETERS</span></span>

### <span data-ttu-id="15c6a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c6a-122">-DefaultProfile</span></span>
<span data-ttu-id="15c6a-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15c6a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15c6a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="15c6a-124">-Force</span></span>
<span data-ttu-id="15c6a-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="15c6a-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="15c6a-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="15c6a-126">-Name</span></span>
<span data-ttu-id="15c6a-127">Anger namnet på den trafik hanterarens slut punkt som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="15c6a-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="15c6a-128">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="15c6a-128">-ProfileName</span></span>
<span data-ttu-id="15c6a-129">Anger namnet på en Traffic Manager-profil där denna cmdlet inaktiverar slut punkter.</span><span class="sxs-lookup"><span data-stu-id="15c6a-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="15c6a-130">Använd Get-AzTrafficManagerProfile cmdlet för att få en profil.</span><span class="sxs-lookup"><span data-stu-id="15c6a-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="15c6a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15c6a-131">-ResourceGroupName</span></span>
<span data-ttu-id="15c6a-132">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="15c6a-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="15c6a-133">Denna cmdlet inaktiverar en hanterings slut punkt för trafik i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="15c6a-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="15c6a-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15c6a-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="15c6a-135">Anger den trafik hanterarens slut punkt som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="15c6a-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="15c6a-136">För att hämta ett **TrafficManagerEndpoint** -objekt, Använd cmdleten Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="15c6a-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="15c6a-137">– Skriv</span><span class="sxs-lookup"><span data-stu-id="15c6a-137">-Type</span></span>
<span data-ttu-id="15c6a-138">Anger den typ av slut punkt som denna cmdlet lägger till i Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="15c6a-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="15c6a-139">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="15c6a-139">Valid values are:</span></span> 

- <span data-ttu-id="15c6a-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="15c6a-140">AzureEndpoints</span></span>
- <span data-ttu-id="15c6a-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="15c6a-141">ExternalEndpoints</span></span>
- <span data-ttu-id="15c6a-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="15c6a-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="15c6a-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="15c6a-143">-Confirm</span></span>
<span data-ttu-id="15c6a-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="15c6a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15c6a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15c6a-145">-WhatIf</span></span>
<span data-ttu-id="15c6a-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="15c6a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15c6a-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="15c6a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15c6a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c6a-148">CommonParameters</span></span>
<span data-ttu-id="15c6a-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15c6a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c6a-150">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15c6a-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c6a-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15c6a-151">INPUTS</span></span>

### <span data-ttu-id="15c6a-152">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15c6a-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="15c6a-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15c6a-153">OUTPUTS</span></span>

### <span data-ttu-id="15c6a-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15c6a-154">System.Boolean</span></span>

## <span data-ttu-id="15c6a-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15c6a-155">NOTES</span></span>

## <span data-ttu-id="15c6a-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15c6a-156">RELATED LINKS</span></span>

[<span data-ttu-id="15c6a-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15c6a-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="15c6a-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15c6a-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="15c6a-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="15c6a-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="15c6a-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15c6a-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="15c6a-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="15c6a-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="15c6a-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15c6a-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="15c6a-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="15c6a-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


