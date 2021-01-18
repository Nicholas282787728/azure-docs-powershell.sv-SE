---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523882"
---
# <span data-ttu-id="a7f4d-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a7f4d-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="a7f4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f4d-103">Uppdaterar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="a7f4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7f4d-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7f4d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7f4d-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f4d-106">Cmdleten **set-AzTrafficManagerProfile** uppdaterar en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="a7f4d-107">Denna cmdlet uppdaterar inställningarna för profilen från ett lokalt profil objekt.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="a7f4d-108">Du kan ange ett profil objekt antingen med hjälp av parametern *TrafficManagerProfile* eller genom att använda pipeline.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="a7f4d-109">Du kan få ett lokalt objekt som representerar en profil med hjälp av Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="a7f4d-110">Ändra objektet lokalt och Använd sedan **set-AzTrafficManagerProfile** för att bekräfta dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="a7f4d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7f4d-111">EXAMPLES</span></span>

### <span data-ttu-id="a7f4d-112">Exempel 1: uppdatera en profil</span><span class="sxs-lookup"><span data-stu-id="a7f4d-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="a7f4d-113">Det första kommandot får en Azure Traffic Manager-profil med hjälp av Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="a7f4d-114">Kommandot lagrar profilen lokalt i $TrafficManagerProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="a7f4d-115">Det andra kommandot ändrar profilen lokalt.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="a7f4d-116">Det här kommandot inaktiverar profilen.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-116">This command disables the profile.</span></span>

<span data-ttu-id="a7f4d-117">Det tredje kommandot uppdaterar Traffic Manager-profilen med namnet ContosoProfile för att matcha det lokala värdet i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="a7f4d-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7f4d-118">PARAMETERS</span></span>

### <span data-ttu-id="a7f4d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f4d-119">-DefaultProfile</span></span>
<span data-ttu-id="a7f4d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7f4d-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a7f4d-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="a7f4d-122">Anger ett lokalt **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="a7f4d-123">Denna cmdlet uppdaterar trafik hanteraren så att den matchar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="a7f4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f4d-124">CommonParameters</span></span>
<span data-ttu-id="a7f4d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f4d-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7f4d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f4d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7f4d-127">INPUTS</span></span>

### <span data-ttu-id="a7f4d-128">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a7f4d-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="a7f4d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7f4d-129">OUTPUTS</span></span>

### <span data-ttu-id="a7f4d-130">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a7f4d-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="a7f4d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7f4d-131">NOTES</span></span>

## <span data-ttu-id="a7f4d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7f4d-132">RELATED LINKS</span></span>

[<span data-ttu-id="a7f4d-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="a7f4d-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="a7f4d-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a7f4d-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="a7f4d-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a7f4d-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="a7f4d-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="a7f4d-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="a7f4d-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a7f4d-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


