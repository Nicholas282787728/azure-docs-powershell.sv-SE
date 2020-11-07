---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 99915859798eba5acb78fc62a5a5c56cff2ce791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919510"
---
# <span data-ttu-id="a3f2f-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3f2f-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="a3f2f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f2f-103">Aktiverar en slut punkt i en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="a3f2f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3f2f-104">SYNTAX</span></span>

### <span data-ttu-id="a3f2f-105">Fält</span><span class="sxs-lookup"><span data-stu-id="a3f2f-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3f2f-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="a3f2f-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3f2f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3f2f-107">DESCRIPTION</span></span>
<span data-ttu-id="a3f2f-108">Cmdleten **Enable-AzTrafficManagerEndpoint** aktiverar en slut punkt i en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="a3f2f-109">Du kan använda pipeline-operatorn för att skicka ett **TrafficManagerEndpoint** -objekt till denna cmdlet, eller så kan du ange ett **TrafficManagerEndpoint** -objekt med hjälp av parametern *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="a3f2f-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="a3f2f-110">Alternativt kan du ange slut punktens namn och typ genom att använda parametrarna *Name* och *Type* tillsammans med parametrarna *Profilnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a3f2f-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="a3f2f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3f2f-111">EXAMPLES</span></span>

### <span data-ttu-id="a3f2f-112">Exempel 1: Aktivera en slut punkt från en profil</span><span class="sxs-lookup"><span data-stu-id="a3f2f-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="a3f2f-113">Med det här kommandot aktive ras den externa slut punkten contoso i profilen med namnet ContosoProfile i resurs grupp ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="a3f2f-114">Exempel 2: Aktivera en slut punkt genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="a3f2f-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="a3f2f-115">Det här kommandot får den externa slut punkten namnet contoso från den profil som heter ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="a3f2f-116">Kommandot skickar sedan slut punkten till cmdleten **Enable-AzTrafficManagerEndpoint** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a3f2f-117">Denna cmdlet aktiverar slut punkten.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="a3f2f-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3f2f-118">PARAMETERS</span></span>

### <span data-ttu-id="a3f2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f2f-119">-DefaultProfile</span></span>
<span data-ttu-id="a3f2f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3f2f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a3f2f-121">-Name</span></span>
<span data-ttu-id="a3f2f-122">Anger namnet på den trafik hanterarens slut punkt som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="a3f2f-123">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="a3f2f-123">-ProfileName</span></span>
<span data-ttu-id="a3f2f-124">Anger namnet på en Traffic Manager-profil där denna cmdlet aktiverar en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="a3f2f-125">Använd Get-AzTrafficManagerProfile cmdlet för att få en profil.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="a3f2f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3f2f-126">-ResourceGroupName</span></span>
<span data-ttu-id="a3f2f-127">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a3f2f-128">Denna cmdlet aktiverar en hanterings slut punkt för trafik i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3f2f-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3f2f-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="a3f2f-130">Anger den trafik hanterarens slut punkt som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="a3f2f-131">För att hämta ett **TrafficManagerEndpoint** -objekt, Använd cmdleten Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="a3f2f-132">– Skriv</span><span class="sxs-lookup"><span data-stu-id="a3f2f-132">-Type</span></span>
<span data-ttu-id="a3f2f-133">Anger den typ av slut punkt som denna cmdlet inaktiverar i Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="a3f2f-134">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a3f2f-134">Valid values are:</span></span> 

- <span data-ttu-id="a3f2f-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="a3f2f-135">AzureEndpoints</span></span>
- <span data-ttu-id="a3f2f-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="a3f2f-136">ExternalEndpoints</span></span>
- <span data-ttu-id="a3f2f-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="a3f2f-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="a3f2f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f2f-138">CommonParameters</span></span>
<span data-ttu-id="a3f2f-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3f2f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f2f-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3f2f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f2f-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3f2f-141">INPUTS</span></span>

### <span data-ttu-id="a3f2f-142">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3f2f-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a3f2f-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3f2f-143">OUTPUTS</span></span>

### <span data-ttu-id="a3f2f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3f2f-144">System.Boolean</span></span>

## <span data-ttu-id="a3f2f-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3f2f-145">NOTES</span></span>

## <span data-ttu-id="a3f2f-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3f2f-146">RELATED LINKS</span></span>

[<span data-ttu-id="a3f2f-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3f2f-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a3f2f-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3f2f-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a3f2f-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a3f2f-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="a3f2f-150">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3f2f-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a3f2f-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a3f2f-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="a3f2f-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3f2f-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a3f2f-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a3f2f-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


