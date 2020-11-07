---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 13b798da7b35a4721b35d2375cf4e25bb47fbb98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756434"
---
# <span data-ttu-id="73f77-101">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="73f77-101">Disable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="73f77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73f77-102">SYNOPSIS</span></span>
<span data-ttu-id="73f77-103">Inaktiverar en slut punkt i en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="73f77-103">Disables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73f77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73f77-104">SYNTAX</span></span>

### <span data-ttu-id="73f77-105">Fält</span><span class="sxs-lookup"><span data-stu-id="73f77-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73f77-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="73f77-106">Object</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73f77-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73f77-107">DESCRIPTION</span></span>
<span data-ttu-id="73f77-108">Cmdleten **disable-AzureRmTrafficManagerEndpoint** inaktiverar en slut punkt i en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="73f77-108">The **Disable-AzureRmTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="73f77-109">Du kan använda pipeline-operatorn för att skicka ett **TrafficManagerEndpoint** -objekt till denna cmdlet, eller så kan du skicka ett **TrafficManagerEndpoint** -objekt med parametern *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="73f77-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="73f77-110">Alternativt kan du ange slut punktens namn och typ genom att använda parametrarna *Name* och *Type* tillsammans med parametrarna *Profilnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="73f77-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="73f77-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73f77-111">EXAMPLES</span></span>

### <span data-ttu-id="73f77-112">Exempel 1: inaktivera en slut punkt efter namn</span><span class="sxs-lookup"><span data-stu-id="73f77-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="73f77-113">Det här kommandot inaktiverar den externa slut punkten med namnet contoso i profilen med namnet ContosoProfile i resurs gruppen ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="73f77-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="73f77-114">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="73f77-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="73f77-115">Exempel 2: inaktivera en slut punkt genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="73f77-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

<span data-ttu-id="73f77-116">Det här kommandot får den externa slut punkten namnet contoso från den profil som heter ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="73f77-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="73f77-117">Kommandot skickar sedan slut punkten till cmdleten **disable-AzureRmTrafficManagerEndpoint** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="73f77-117">The command then passes that endpoint to the **Disable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="73f77-118">Denna cmdlet inaktiverar slut punkten.</span><span class="sxs-lookup"><span data-stu-id="73f77-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="73f77-119">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="73f77-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="73f77-120">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="73f77-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="73f77-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73f77-121">PARAMETERS</span></span>

### <span data-ttu-id="73f77-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f77-122">-DefaultProfile</span></span>
<span data-ttu-id="73f77-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73f77-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f77-124">-Force</span><span class="sxs-lookup"><span data-stu-id="73f77-124">-Force</span></span>
<span data-ttu-id="73f77-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="73f77-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f77-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="73f77-126">-Name</span></span>
<span data-ttu-id="73f77-127">Anger namnet på den trafik hanterarens slut punkt som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="73f77-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f77-128">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="73f77-128">-ProfileName</span></span>
<span data-ttu-id="73f77-129">Anger namnet på en Traffic Manager-profil där denna cmdlet inaktiverar slut punkter.</span><span class="sxs-lookup"><span data-stu-id="73f77-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="73f77-130">Använd Get-AzureRmTrafficManagerProfile cmdlet för att få en profil.</span><span class="sxs-lookup"><span data-stu-id="73f77-130">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f77-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73f77-131">-ResourceGroupName</span></span>
<span data-ttu-id="73f77-132">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="73f77-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="73f77-133">Denna cmdlet inaktiverar en hanterings slut punkt för trafik i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="73f77-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f77-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="73f77-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="73f77-135">Anger den trafik hanterarens slut punkt som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="73f77-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="73f77-136">För att hämta ett **TrafficManagerEndpoint** -objekt, Använd cmdleten Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="73f77-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73f77-137">– Skriv</span><span class="sxs-lookup"><span data-stu-id="73f77-137">-Type</span></span>
<span data-ttu-id="73f77-138">Anger den typ av slut punkt som denna cmdlet lägger till i Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="73f77-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="73f77-139">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="73f77-139">Valid values are:</span></span> 

- <span data-ttu-id="73f77-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="73f77-140">AzureEndpoints</span></span>
- <span data-ttu-id="73f77-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="73f77-141">ExternalEndpoints</span></span>
- <span data-ttu-id="73f77-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="73f77-142">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f77-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="73f77-143">-Confirm</span></span>
<span data-ttu-id="73f77-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73f77-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f77-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73f77-145">-WhatIf</span></span>
<span data-ttu-id="73f77-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="73f77-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73f77-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="73f77-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f77-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f77-148">CommonParameters</span></span>
<span data-ttu-id="73f77-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f77-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f77-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73f77-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f77-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73f77-151">INPUTS</span></span>

### <span data-ttu-id="73f77-152">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="73f77-152">TrafficManagerEndpoint</span></span>
<span data-ttu-id="73f77-153">Parametern ' TrafficManagerEndpoint ' godkänner värdet av typen ' TrafficManagerEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="73f77-153">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="73f77-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73f77-154">OUTPUTS</span></span>

### <span data-ttu-id="73f77-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73f77-155">System.Boolean</span></span>

## <span data-ttu-id="73f77-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73f77-156">NOTES</span></span>

## <span data-ttu-id="73f77-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73f77-157">RELATED LINKS</span></span>

[<span data-ttu-id="73f77-158">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="73f77-158">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="73f77-159">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="73f77-159">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="73f77-160">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="73f77-160">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="73f77-161">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="73f77-161">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="73f77-162">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="73f77-162">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="73f77-163">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="73f77-163">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="73f77-164">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="73f77-164">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


