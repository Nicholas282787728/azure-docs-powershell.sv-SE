---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 1481b577e248354eb2fdccbb9d6ecd450ab0cf62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586456"
---
# <span data-ttu-id="af7c9-101">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7c9-101">Disable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="af7c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af7c9-102">SYNOPSIS</span></span>
<span data-ttu-id="af7c9-103">Inaktiverar en slut punkt i en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="af7c9-103">Disables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af7c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af7c9-104">SYNTAX</span></span>

### <span data-ttu-id="af7c9-105">Fält</span><span class="sxs-lookup"><span data-stu-id="af7c9-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af7c9-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="af7c9-106">Object</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af7c9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af7c9-107">DESCRIPTION</span></span>
<span data-ttu-id="af7c9-108">Cmdleten **disable-AzureRmTrafficManagerEndpoint** inaktiverar en slut punkt i en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="af7c9-108">The **Disable-AzureRmTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="af7c9-109">Du kan använda pipeline-operatorn för att skicka ett **TrafficManagerEndpoint** -objekt till denna cmdlet, eller så kan du skicka ett **TrafficManagerEndpoint** -objekt med parametern *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="af7c9-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="af7c9-110">Alternativt kan du ange slut punktens namn och typ genom att använda parametrarna *Name* och *Type* tillsammans med parametrarna *Profilnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="af7c9-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="af7c9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af7c9-111">EXAMPLES</span></span>

### <span data-ttu-id="af7c9-112">Exempel 1: inaktivera en slut punkt efter namn</span><span class="sxs-lookup"><span data-stu-id="af7c9-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="af7c9-113">Det här kommandot inaktiverar den externa slut punkten med namnet contoso i profilen med namnet ContosoProfile i resurs gruppen ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="af7c9-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="af7c9-114">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="af7c9-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="af7c9-115">Exempel 2: inaktivera en slut punkt genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="af7c9-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

<span data-ttu-id="af7c9-116">Det här kommandot får den externa slut punkten namnet contoso från den profil som heter ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="af7c9-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="af7c9-117">Kommandot skickar sedan slut punkten till cmdleten **disable-AzureRmTrafficManagerEndpoint** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="af7c9-117">The command then passes that endpoint to the **Disable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="af7c9-118">Denna cmdlet inaktiverar slut punkten.</span><span class="sxs-lookup"><span data-stu-id="af7c9-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="af7c9-119">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="af7c9-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="af7c9-120">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="af7c9-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="af7c9-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af7c9-121">PARAMETERS</span></span>

### <span data-ttu-id="af7c9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="af7c9-122">-Force</span></span>
<span data-ttu-id="af7c9-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="af7c9-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af7c9-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="af7c9-124">-Name</span></span>
<span data-ttu-id="af7c9-125">Anger namnet på den trafik hanterarens slut punkt som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="af7c9-125">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="af7c9-126">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="af7c9-126">-ProfileName</span></span>
<span data-ttu-id="af7c9-127">Anger namnet på en Traffic Manager-profil där denna cmdlet inaktiverar slut punkter.</span><span class="sxs-lookup"><span data-stu-id="af7c9-127">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="af7c9-128">Använd Get-AzureRmTrafficManagerProfile cmdlet för att få en profil.</span><span class="sxs-lookup"><span data-stu-id="af7c9-128">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="af7c9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af7c9-129">-ResourceGroupName</span></span>
<span data-ttu-id="af7c9-130">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="af7c9-130">Specifies the name of a resource group.</span></span>
<span data-ttu-id="af7c9-131">Denna cmdlet inaktiverar en hanterings slut punkt för trafik i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="af7c9-131">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="af7c9-132">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7c9-132">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="af7c9-133">Anger den trafik hanterarens slut punkt som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="af7c9-133">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="af7c9-134">För att hämta ett **TrafficManagerEndpoint** -objekt, Använd cmdleten Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="af7c9-134">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="af7c9-135">– Skriv</span><span class="sxs-lookup"><span data-stu-id="af7c9-135">-Type</span></span>
<span data-ttu-id="af7c9-136">Anger den typ av slut punkt som denna cmdlet lägger till i Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="af7c9-136">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="af7c9-137">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="af7c9-137">Valid values are:</span></span> 

- <span data-ttu-id="af7c9-138">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="af7c9-138">AzureEndpoints</span></span>
- <span data-ttu-id="af7c9-139">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="af7c9-139">ExternalEndpoints</span></span>
- <span data-ttu-id="af7c9-140">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="af7c9-140">NestedEndpoints</span></span>

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

### <span data-ttu-id="af7c9-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af7c9-141">-Confirm</span></span>
<span data-ttu-id="af7c9-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af7c9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af7c9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af7c9-143">-WhatIf</span></span>
<span data-ttu-id="af7c9-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af7c9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af7c9-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af7c9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af7c9-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7c9-146">-DefaultProfile</span></span>
<span data-ttu-id="af7c9-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af7c9-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af7c9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7c9-148">CommonParameters</span></span>
<span data-ttu-id="af7c9-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af7c9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7c9-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af7c9-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7c9-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af7c9-151">INPUTS</span></span>

### <span data-ttu-id="af7c9-152">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7c9-152">TrafficManagerEndpoint</span></span>
<span data-ttu-id="af7c9-153">Parametern ' TrafficManagerEndpoint ' godkänner värdet av typen ' TrafficManagerEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="af7c9-153">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="af7c9-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af7c9-154">OUTPUTS</span></span>

### <span data-ttu-id="af7c9-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af7c9-155">System.Boolean</span></span>

## <span data-ttu-id="af7c9-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af7c9-156">NOTES</span></span>

## <span data-ttu-id="af7c9-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af7c9-157">RELATED LINKS</span></span>

[<span data-ttu-id="af7c9-158">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7c9-158">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="af7c9-159">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7c9-159">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="af7c9-160">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af7c9-160">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="af7c9-161">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7c9-161">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="af7c9-162">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af7c9-162">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="af7c9-163">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7c9-163">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="af7c9-164">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af7c9-164">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


