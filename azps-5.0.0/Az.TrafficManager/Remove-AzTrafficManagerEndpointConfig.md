---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4795e89013acaadcc08477370441ff5acdded85a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271675"
---
# <span data-ttu-id="e5976-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="e5976-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="e5976-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5976-102">SYNOPSIS</span></span>
<span data-ttu-id="e5976-103">Tar bort en slut punkt från ett lokalt Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="e5976-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="e5976-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5976-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5976-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5976-105">DESCRIPTION</span></span>
<span data-ttu-id="e5976-106">Cmdleten **Remove-AzTrafficManagerEndpointConfig** tar bort en slut punkt från ett lokalt Azure Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="e5976-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="e5976-107">Du kan hämta en profil med hjälp av Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5976-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="e5976-108">Denna cmdlet fungerar på det lokala profilens objekt.</span><span class="sxs-lookup"><span data-stu-id="e5976-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="e5976-109">Bekräfta dina ändringar av profilen för Traffic Manager genom att använda Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5976-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="e5976-110">Om du vill ta bort en slut punkt och verkställa ändringar i en enskild åtgärd kan du använda Remove-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5976-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="e5976-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5976-111">EXAMPLES</span></span>

### <span data-ttu-id="e5976-112">Exempel 1: ta bort en slut punkt</span><span class="sxs-lookup"><span data-stu-id="e5976-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="e5976-113">Det första kommandot får en Azure Traffic Manager-profil genom att använda cmdleten **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="e5976-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="e5976-114">Kommandot lagrar den lokala profilen i $TrafficManagerProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="e5976-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="e5976-115">Det andra kommandot tar bort en Azure-slutpunkt med namnet contoso från profilen som lagras i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e5976-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="e5976-116">Det här kommandot ändrar bara det lokala objektet.</span><span class="sxs-lookup"><span data-stu-id="e5976-116">This command changes only the local object.</span></span>

<span data-ttu-id="e5976-117">Det sista kommandot uppdaterar Traffic Manager-profilen med namnet ContosoProfile för att matcha det lokala värdet i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e5976-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="e5976-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5976-118">PARAMETERS</span></span>

### <span data-ttu-id="e5976-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5976-119">-DefaultProfile</span></span>
<span data-ttu-id="e5976-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5976-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5976-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e5976-121">-EndpointName</span></span>
<span data-ttu-id="e5976-122">Anger namnet på den trafik hanterarens slut punkt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="e5976-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5976-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e5976-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="e5976-124">Anger ett lokalt **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e5976-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="e5976-125">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="e5976-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="e5976-126">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e5976-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5976-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5976-127">CommonParameters</span></span>
<span data-ttu-id="e5976-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5976-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5976-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5976-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5976-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5976-130">INPUTS</span></span>

### <span data-ttu-id="e5976-131">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e5976-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="e5976-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5976-132">OUTPUTS</span></span>

### <span data-ttu-id="e5976-133">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e5976-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="e5976-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5976-134">NOTES</span></span>

## <span data-ttu-id="e5976-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5976-135">RELATED LINKS</span></span>

[<span data-ttu-id="e5976-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="e5976-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="e5976-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e5976-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="e5976-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5976-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e5976-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e5976-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

