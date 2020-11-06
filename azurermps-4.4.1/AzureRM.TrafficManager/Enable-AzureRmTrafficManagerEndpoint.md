---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 64fdd0cb3c2fa31396d9e917dcd7c2e26730c755
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573614"
---
# <span data-ttu-id="fe763-101">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe763-101">Enable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="fe763-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe763-102">SYNOPSIS</span></span>
<span data-ttu-id="fe763-103">Aktiverar en slut punkt i en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="fe763-103">Enables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe763-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe763-104">SYNTAX</span></span>

### <span data-ttu-id="fe763-105">Fält</span><span class="sxs-lookup"><span data-stu-id="fe763-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe763-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="fe763-106">Object</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe763-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe763-107">DESCRIPTION</span></span>
<span data-ttu-id="fe763-108">Cmdleten **Enable-AzureRmTrafficManagerEndpoint** aktiverar en slut punkt i en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="fe763-108">The **Enable-AzureRmTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="fe763-109">Du kan använda pipeline-operatorn för att skicka ett **TrafficManagerEndpoint** -objekt till denna cmdlet, eller så kan du ange ett **TrafficManagerEndpoint** -objekt med hjälp av parametern *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="fe763-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="fe763-110">Alternativt kan du ange slut punktens namn och typ genom att använda parametrarna *Name* och *Type* tillsammans med parametrarna *Profilnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="fe763-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="fe763-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe763-111">EXAMPLES</span></span>

### <span data-ttu-id="fe763-112">Exempel 1: Aktivera en slut punkt från en profil</span><span class="sxs-lookup"><span data-stu-id="fe763-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="fe763-113">Med det här kommandot aktive ras den externa slut punkten contoso i profilen med namnet ContosoProfile i resurs grupp ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fe763-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>

### <span data-ttu-id="fe763-114">Exempel 2: Aktivera en slut punkt genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="fe763-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerEndpoint
```

<span data-ttu-id="fe763-115">Det här kommandot får den externa slut punkten namnet contoso från den profil som heter ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fe763-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="fe763-116">Kommandot skickar sedan slut punkten till cmdleten **Enable-AzureRmTrafficManagerEndpoint** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="fe763-116">The command then passes that endpoint to the **Enable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fe763-117">Denna cmdlet aktiverar slut punkten.</span><span class="sxs-lookup"><span data-stu-id="fe763-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="fe763-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe763-118">PARAMETERS</span></span>

### <span data-ttu-id="fe763-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe763-119">-Name</span></span>
<span data-ttu-id="fe763-120">Anger namnet på den trafik hanterarens slut punkt som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="fe763-120">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="fe763-121">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="fe763-121">-ProfileName</span></span>
<span data-ttu-id="fe763-122">Anger namnet på en Traffic Manager-profil där denna cmdlet aktiverar en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="fe763-122">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="fe763-123">Använd Get-AzureRmTrafficManagerProfile cmdlet för att få en profil.</span><span class="sxs-lookup"><span data-stu-id="fe763-123">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="fe763-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe763-124">-ResourceGroupName</span></span>
<span data-ttu-id="fe763-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="fe763-125">Specifies the name of a resource group.</span></span>
<span data-ttu-id="fe763-126">Denna cmdlet aktiverar en hanterings slut punkt för trafik i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fe763-126">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fe763-127">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe763-127">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="fe763-128">Anger den trafik hanterarens slut punkt som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="fe763-128">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="fe763-129">För att hämta ett **TrafficManagerEndpoint** -objekt, Använd cmdleten Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="fe763-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="fe763-130">– Skriv</span><span class="sxs-lookup"><span data-stu-id="fe763-130">-Type</span></span>
<span data-ttu-id="fe763-131">Anger den typ av slut punkt som denna cmdlet inaktiverar i Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="fe763-131">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="fe763-132">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="fe763-132">Valid values are:</span></span> 

- <span data-ttu-id="fe763-133">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="fe763-133">AzureEndpoints</span></span>
- <span data-ttu-id="fe763-134">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="fe763-134">ExternalEndpoints</span></span>
- <span data-ttu-id="fe763-135">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="fe763-135">NestedEndpoints</span></span>

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

### <span data-ttu-id="fe763-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe763-136">-DefaultProfile</span></span>
<span data-ttu-id="fe763-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe763-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe763-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe763-138">CommonParameters</span></span>
<span data-ttu-id="fe763-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe763-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe763-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe763-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe763-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe763-141">INPUTS</span></span>

### <span data-ttu-id="fe763-142">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe763-142">TrafficManagerEndpoint</span></span>
<span data-ttu-id="fe763-143">Parametern ' TrafficManagerEndpoint ' godkänner värdet av typen ' TrafficManagerEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fe763-143">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="fe763-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe763-144">OUTPUTS</span></span>

### <span data-ttu-id="fe763-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe763-145">System.Boolean</span></span>

## <span data-ttu-id="fe763-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe763-146">NOTES</span></span>

## <span data-ttu-id="fe763-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe763-147">RELATED LINKS</span></span>

[<span data-ttu-id="fe763-148">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe763-148">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="fe763-149">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe763-149">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="fe763-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fe763-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fe763-151">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe763-151">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="fe763-152">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fe763-152">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fe763-153">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe763-153">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="fe763-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fe763-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


