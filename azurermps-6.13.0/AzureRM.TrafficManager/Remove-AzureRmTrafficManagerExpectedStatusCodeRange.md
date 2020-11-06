---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 0971a4b8d485c1590794de6f1b6c2d4d9d21da4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573838"
---
# <span data-ttu-id="a9496-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="a9496-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="a9496-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9496-102">SYNOPSIS</span></span>
<span data-ttu-id="a9496-103">Tar bort ett förväntat status kods område från ett lokalt Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="a9496-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9496-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9496-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9496-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9496-105">DESCRIPTION</span></span>
<span data-ttu-id="a9496-106">Cmdleten **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** tar bort ett intervall med förväntade status koder från ett lokalt Azure Traffic Manager-profil objekt.</span><span class="sxs-lookup"><span data-stu-id="a9496-106">The **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="a9496-107">Du kan hämta en profil med hjälp av New-AzureRmTrafficManagerProfile eller Get-AzureRmTrafficManagerProfile cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a9496-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="a9496-108">Denna cmdlet fungerar på det lokala profilens objekt.</span><span class="sxs-lookup"><span data-stu-id="a9496-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="a9496-109">Bekräfta dina ändringar av profilen för Traffic Manager genom att använda Set-AzureRmTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9496-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="a9496-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9496-110">EXAMPLES</span></span>

### <span data-ttu-id="a9496-111">Exempel 1: ta bort ett intervall med status koder från en profil</span><span class="sxs-lookup"><span data-stu-id="a9496-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="a9496-112">Det första kommandot får en Azure Traffic Manager-profil genom att använda cmdleten **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="a9496-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="a9496-113">Med det andra kommandot tas ett förväntat status kods område bort från profilen som lagras i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a9496-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="a9496-114">Kommandot uppdaterar profilen i Traffic Manager så att den matchar det lokala värdet i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a9496-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="a9496-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9496-115">PARAMETERS</span></span>

### <span data-ttu-id="a9496-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9496-116">-DefaultProfile</span></span>
<span data-ttu-id="a9496-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9496-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9496-118">-Min</span><span class="sxs-lookup"><span data-stu-id="a9496-118">-Min</span></span>
<span data-ttu-id="a9496-119">Anger det lägsta värdet i intervallet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a9496-119">Specifies the lowest value in the status code range to be removed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9496-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a9496-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="a9496-121">Anger ett lokalt **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a9496-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="a9496-122">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="a9496-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="a9496-123">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a9496-123">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="a9496-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9496-124">-Confirm</span></span>
<span data-ttu-id="a9496-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9496-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9496-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9496-126">-WhatIf</span></span>
<span data-ttu-id="a9496-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9496-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9496-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a9496-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9496-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9496-129">CommonParameters</span></span>
<span data-ttu-id="a9496-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9496-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9496-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9496-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9496-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9496-132">INPUTS</span></span>

### <span data-ttu-id="a9496-133">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a9496-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="a9496-134">Denna cmdlet accepterar ett **TrafficManagerProfile** -objekt till denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9496-134">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="a9496-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9496-135">OUTPUTS</span></span>

### <span data-ttu-id="a9496-136">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a9496-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="a9496-137">Denna cmdlet returnerar ett ändrat **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a9496-137">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="a9496-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9496-138">NOTES</span></span>

## <span data-ttu-id="a9496-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9496-139">RELATED LINKS</span></span>

[<span data-ttu-id="a9496-140">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="a9496-140">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="a9496-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a9496-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a9496-142">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a9496-142">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
