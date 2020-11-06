---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 488643c8f977fb59af0f5b73c9388e65b3425c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580919"
---
# <span data-ttu-id="ac26c-101">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac26c-101">Get-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="ac26c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac26c-102">SYNOPSIS</span></span>
<span data-ttu-id="ac26c-103">Hämtar en slut punkt för en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="ac26c-103">Gets an endpoint for a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac26c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac26c-104">SYNTAX</span></span>

### <span data-ttu-id="ac26c-105">Fält</span><span class="sxs-lookup"><span data-stu-id="ac26c-105">Fields</span></span>
```
Get-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac26c-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="ac26c-106">Object</span></span>
```
Get-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac26c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac26c-107">DESCRIPTION</span></span>
<span data-ttu-id="ac26c-108">Cmdleten **Get-AzureRmTrafficManagerEndpoint** får en slut punkt för en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="ac26c-108">The **Get-AzureRmTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="ac26c-109">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på profilen med hjälp av Set-AzureRmTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac26c-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="ac26c-110">Ange slut punkten genom att använda parametrarna *Name* och *Type* .</span><span class="sxs-lookup"><span data-stu-id="ac26c-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="ac26c-111">Du kan ange Traffic Manager-profilen med hjälp av *PROFILENAME* -och *ResourceGroupName* -parametern, eller genom att ange ett **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ac26c-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="ac26c-112">Alternativt kan du överföra värdet med hjälp av försäljnings förloppet.</span><span class="sxs-lookup"><span data-stu-id="ac26c-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="ac26c-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac26c-113">EXAMPLES</span></span>

### <span data-ttu-id="ac26c-114">Exempel 1: Hämta en slut punkt</span><span class="sxs-lookup"><span data-stu-id="ac26c-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="ac26c-115">Det här kommandot får Azure-slutpunkten contoso från den profil som heter ContosoProfile i resurs gruppen med namnet ResourceGroup11 och lagrar sedan objektet i $TrafficManagerEndpoint variabel.</span><span class="sxs-lookup"><span data-stu-id="ac26c-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="ac26c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac26c-116">PARAMETERS</span></span>

### <span data-ttu-id="ac26c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac26c-117">-DefaultProfile</span></span>
<span data-ttu-id="ac26c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac26c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac26c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac26c-119">-Name</span></span>
<span data-ttu-id="ac26c-120">Anger namnet på den trafik hanterarens slut punkt som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="ac26c-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ac26c-121">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="ac26c-121">-ProfileName</span></span>
<span data-ttu-id="ac26c-122">Anger namnet på den trafik hanterarens slut punkt som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="ac26c-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ac26c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac26c-123">-ResourceGroupName</span></span>
<span data-ttu-id="ac26c-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ac26c-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ac26c-125">Denna cmdlet hämtar en hanterings slut punkt för trafik i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ac26c-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac26c-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac26c-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="ac26c-127">Anger den trafik hanterarens slut punkt som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="ac26c-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ac26c-128">– Skriv</span><span class="sxs-lookup"><span data-stu-id="ac26c-128">-Type</span></span>
<span data-ttu-id="ac26c-129">Anger den typ av slut punkt som denna cmdlet lägger till i Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="ac26c-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="ac26c-130">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="ac26c-130">Valid values are:</span></span> 

- <span data-ttu-id="ac26c-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="ac26c-131">AzureEndpoints</span></span>
- <span data-ttu-id="ac26c-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="ac26c-132">ExternalEndpoints</span></span>
- <span data-ttu-id="ac26c-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="ac26c-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="ac26c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac26c-134">CommonParameters</span></span>
<span data-ttu-id="ac26c-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac26c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac26c-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac26c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac26c-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac26c-137">INPUTS</span></span>

### <span data-ttu-id="ac26c-138">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac26c-138">TrafficManagerEndpoint</span></span>
<span data-ttu-id="ac26c-139">Parametern ' TrafficManagerEndpoint ' godkänner värdet av typen ' TrafficManagerEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ac26c-139">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="ac26c-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac26c-140">OUTPUTS</span></span>

### <span data-ttu-id="ac26c-141">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac26c-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ac26c-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac26c-142">NOTES</span></span>

## <span data-ttu-id="ac26c-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac26c-143">RELATED LINKS</span></span>

[<span data-ttu-id="ac26c-144">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac26c-144">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ac26c-145">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac26c-145">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ac26c-146">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac26c-146">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ac26c-147">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac26c-147">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ac26c-148">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac26c-148">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)


