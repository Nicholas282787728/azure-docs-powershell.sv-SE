---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 58811a34a2f3d2b4684813c42723a5cab354a13f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581887"
---
# <span data-ttu-id="f237c-101">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f237c-101">Set-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="f237c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f237c-102">SYNOPSIS</span></span>
<span data-ttu-id="f237c-103">Uppdaterar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="f237c-103">Updates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f237c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f237c-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f237c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f237c-105">DESCRIPTION</span></span>
<span data-ttu-id="f237c-106">Cmdleten **set-AzureRmTrafficManagerProfile** uppdaterar en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="f237c-106">The **Set-AzureRmTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f237c-107">Denna cmdlet uppdaterar inställningarna för profilen från ett lokalt profil objekt.</span><span class="sxs-lookup"><span data-stu-id="f237c-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="f237c-108">Du kan ange ett profil objekt antingen med hjälp av parametern *TrafficManagerProfile* eller genom att använda pipeline.</span><span class="sxs-lookup"><span data-stu-id="f237c-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="f237c-109">Du kan få ett lokalt objekt som representerar en profil med hjälp av Get-AzureRmTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f237c-109">You can obtain a local object that represents a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f237c-110">Ändra objektet lokalt och Använd sedan **set-AzureRmTrafficManagerProfile** för att bekräfta dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="f237c-110">Modify the object locally and then use **Set-AzureRmTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="f237c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f237c-111">EXAMPLES</span></span>

### <span data-ttu-id="f237c-112">Exempel 1: uppdatera en profil</span><span class="sxs-lookup"><span data-stu-id="f237c-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f237c-113">Det första kommandot får en Azure Traffic Manager-profil med hjälp av Get-AzureRmTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f237c-113">The first command gets an Azure Traffic Manager profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f237c-114">Kommandot lagrar profilen lokalt i $TrafficManagerProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="f237c-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="f237c-115">Det andra kommandot ändrar profilen lokalt.</span><span class="sxs-lookup"><span data-stu-id="f237c-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="f237c-116">Det här kommandot inaktiverar profilen.</span><span class="sxs-lookup"><span data-stu-id="f237c-116">This command disables the profile.</span></span>

<span data-ttu-id="f237c-117">Det tredje kommandot uppdaterar Traffic Manager-profilen med namnet ContosoProfile för att matcha det lokala värdet i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f237c-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f237c-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f237c-118">PARAMETERS</span></span>

### <span data-ttu-id="f237c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f237c-119">-DefaultProfile</span></span>
<span data-ttu-id="f237c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f237c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f237c-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f237c-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="f237c-122">Anger ett lokalt **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f237c-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f237c-123">Denna cmdlet uppdaterar trafik hanteraren så att den matchar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="f237c-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="f237c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f237c-124">CommonParameters</span></span>
<span data-ttu-id="f237c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f237c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f237c-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f237c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f237c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f237c-127">INPUTS</span></span>

### <span data-ttu-id="f237c-128">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f237c-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="f237c-129">Denna cmdlet accepterar ett **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f237c-129">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="f237c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f237c-130">OUTPUTS</span></span>

### <span data-ttu-id="f237c-131">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f237c-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="f237c-132">Denna cmdlet returnerar ett **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f237c-132">This cmdlet returns a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="f237c-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f237c-133">NOTES</span></span>

## <span data-ttu-id="f237c-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f237c-134">RELATED LINKS</span></span>

[<span data-ttu-id="f237c-135">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f237c-135">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f237c-136">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f237c-136">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f237c-137">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f237c-137">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f237c-138">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f237c-138">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f237c-139">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f237c-139">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)


