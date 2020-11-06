---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 7944328c7cac37d88cf18d715cbb7a893eacc683
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576377"
---
# <span data-ttu-id="b5980-101">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b5980-101">Remove-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="b5980-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5980-102">SYNOPSIS</span></span>
<span data-ttu-id="b5980-103">Tar bort en slut punkt från ett lokalt Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="b5980-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5980-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5980-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5980-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5980-105">DESCRIPTION</span></span>
<span data-ttu-id="b5980-106">Cmdleten **Remove-AzureRmTrafficManagerEndpointConfig** tar bort en slut punkt från ett lokalt Azure Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="b5980-106">The **Remove-AzureRmTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="b5980-107">Du kan hämta en profil med hjälp av Get-AzureRmTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5980-107">You can get a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="b5980-108">Denna cmdlet fungerar på det lokala profilens objekt.</span><span class="sxs-lookup"><span data-stu-id="b5980-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="b5980-109">Bekräfta dina ändringar av profilen för Traffic Manager genom att använda Set-AzureRmTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5980-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="b5980-110">Om du vill ta bort en slut punkt och verkställa ändringar i en enskild åtgärd kan du använda Remove-AzureRmTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5980-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="b5980-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5980-111">EXAMPLES</span></span>

### <span data-ttu-id="b5980-112">Exempel 1: ta bort en slut punkt</span><span class="sxs-lookup"><span data-stu-id="b5980-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -Type AzureEndpoints -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="b5980-113">Det första kommandot får en Azure Traffic Manager-profil genom att använda cmdleten **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="b5980-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="b5980-114">Kommandot lagrar den lokala profilen i $TrafficManagerProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="b5980-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="b5980-115">Det andra kommandot tar bort en Azure-slutpunkt med namnet contoso från profilen som lagras i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b5980-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="b5980-116">Det här kommandot ändrar bara det lokala objektet.</span><span class="sxs-lookup"><span data-stu-id="b5980-116">This command changes only the local object.</span></span>

<span data-ttu-id="b5980-117">Det sista kommandot uppdaterar Traffic Manager-profilen med namnet ContosoProfile för att matcha det lokala värdet i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b5980-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="b5980-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5980-118">PARAMETERS</span></span>

### <span data-ttu-id="b5980-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5980-119">-DefaultProfile</span></span>
<span data-ttu-id="b5980-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5980-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5980-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b5980-121">-EndpointName</span></span>
<span data-ttu-id="b5980-122">Anger namnet på den trafik hanterarens slut punkt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="b5980-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5980-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b5980-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="b5980-124">Anger ett lokalt **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b5980-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="b5980-125">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="b5980-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="b5980-126">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b5980-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5980-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5980-127">CommonParameters</span></span>
<span data-ttu-id="b5980-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5980-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5980-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5980-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5980-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5980-130">INPUTS</span></span>

### <span data-ttu-id="b5980-131">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b5980-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="b5980-132">Denna cmdlet accepterar ett **TrafficManagerProfile** -objekt till denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5980-132">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="b5980-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5980-133">OUTPUTS</span></span>

### <span data-ttu-id="b5980-134">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b5980-134">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="b5980-135">Denna cmdlet returnerar ett ändrat TrafficManagerProfile-objekt.</span><span class="sxs-lookup"><span data-stu-id="b5980-135">This cmdlet returns a modified TrafficManagerProfile object.</span></span>

## <span data-ttu-id="b5980-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5980-136">NOTES</span></span>

## <span data-ttu-id="b5980-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5980-137">RELATED LINKS</span></span>

[<span data-ttu-id="b5980-138">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b5980-138">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="b5980-139">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b5980-139">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b5980-140">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5980-140">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b5980-141">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b5980-141">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


