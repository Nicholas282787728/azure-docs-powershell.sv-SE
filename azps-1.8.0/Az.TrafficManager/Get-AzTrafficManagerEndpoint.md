---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9ac1bb863053fc322265613a24d90b700d1846cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746130"
---
# <span data-ttu-id="03802-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="03802-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="03802-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03802-102">SYNOPSIS</span></span>
<span data-ttu-id="03802-103">Hämtar en slut punkt för en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="03802-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="03802-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03802-104">SYNTAX</span></span>

### <span data-ttu-id="03802-105">Fält</span><span class="sxs-lookup"><span data-stu-id="03802-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03802-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="03802-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03802-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03802-107">DESCRIPTION</span></span>
<span data-ttu-id="03802-108">Cmdleten **Get-AzTrafficManagerEndpoint** får en slut punkt för en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="03802-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="03802-109">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på profilen med hjälp av Set-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03802-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="03802-110">Ange slut punkten genom att använda parametrarna *Name* och *Type* .</span><span class="sxs-lookup"><span data-stu-id="03802-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="03802-111">Du kan ange Traffic Manager-profilen med hjälp av *PROFILENAME* -och *ResourceGroupName* -parametern, eller genom att ange ett **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="03802-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="03802-112">Alternativt kan du överföra värdet med hjälp av försäljnings förloppet.</span><span class="sxs-lookup"><span data-stu-id="03802-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="03802-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03802-113">EXAMPLES</span></span>

### <span data-ttu-id="03802-114">Exempel 1: Hämta en slut punkt</span><span class="sxs-lookup"><span data-stu-id="03802-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="03802-115">Det här kommandot får Azure-slutpunkten contoso från den profil som heter ContosoProfile i resurs gruppen med namnet ResourceGroup11 och lagrar sedan objektet i $TrafficManagerEndpoint variabel.</span><span class="sxs-lookup"><span data-stu-id="03802-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="03802-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03802-116">PARAMETERS</span></span>

### <span data-ttu-id="03802-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03802-117">-DefaultProfile</span></span>
<span data-ttu-id="03802-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03802-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03802-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="03802-119">-Name</span></span>
<span data-ttu-id="03802-120">Anger namnet på den trafik hanterarens slut punkt som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="03802-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="03802-121">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="03802-121">-ProfileName</span></span>
<span data-ttu-id="03802-122">Anger namnet på den trafik hanterarens slut punkt som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="03802-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="03802-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03802-123">-ResourceGroupName</span></span>
<span data-ttu-id="03802-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="03802-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="03802-125">Denna cmdlet hämtar en hanterings slut punkt för trafik i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="03802-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="03802-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="03802-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="03802-127">Anger den trafik hanterarens slut punkt som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="03802-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="03802-128">– Skriv</span><span class="sxs-lookup"><span data-stu-id="03802-128">-Type</span></span>
<span data-ttu-id="03802-129">Anger den typ av slut punkt som denna cmdlet lägger till i Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="03802-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="03802-130">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="03802-130">Valid values are:</span></span> 

- <span data-ttu-id="03802-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="03802-131">AzureEndpoints</span></span>
- <span data-ttu-id="03802-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="03802-132">ExternalEndpoints</span></span>
- <span data-ttu-id="03802-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="03802-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="03802-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03802-134">CommonParameters</span></span>
<span data-ttu-id="03802-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03802-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03802-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03802-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03802-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03802-137">INPUTS</span></span>

### <span data-ttu-id="03802-138">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="03802-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="03802-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03802-139">OUTPUTS</span></span>

### <span data-ttu-id="03802-140">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="03802-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="03802-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03802-141">NOTES</span></span>

## <span data-ttu-id="03802-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03802-142">RELATED LINKS</span></span>

[<span data-ttu-id="03802-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="03802-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="03802-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="03802-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="03802-145">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="03802-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="03802-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="03802-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="03802-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="03802-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


