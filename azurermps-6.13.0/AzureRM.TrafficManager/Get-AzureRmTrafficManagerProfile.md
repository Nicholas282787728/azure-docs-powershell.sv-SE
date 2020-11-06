---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 239e0147b1955c59dbe34591f85273f05aa12c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573847"
---
# <span data-ttu-id="df575-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="df575-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="df575-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df575-102">SYNOPSIS</span></span>
<span data-ttu-id="df575-103">Hämtar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="df575-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df575-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df575-104">SYNTAX</span></span>

### <span data-ttu-id="df575-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="df575-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df575-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="df575-106">AccountNameParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df575-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df575-107">DESCRIPTION</span></span>
<span data-ttu-id="df575-108">Cmdleten **Get-AzureRmTrafficManagerProfile** hämtar en Azure Traffic Manager-profil och returnerar ett objekt som representerar den profilen.</span><span class="sxs-lookup"><span data-stu-id="df575-108">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="df575-109">Ange en profil efter dess namn och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="df575-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="df575-110">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på profilen med hjälp av Set-AzureRmTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df575-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="df575-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df575-111">EXAMPLES</span></span>

### <span data-ttu-id="df575-112">Exempel 1: skaffa en profil</span><span class="sxs-lookup"><span data-stu-id="df575-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="df575-113">Det här kommandot får profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="df575-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="df575-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df575-114">PARAMETERS</span></span>

### <span data-ttu-id="df575-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df575-115">-DefaultProfile</span></span>
<span data-ttu-id="df575-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df575-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df575-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="df575-117">-Name</span></span>
<span data-ttu-id="df575-118">Anger namnet på den Traffic Manager-profil som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="df575-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df575-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df575-119">-ResourceGroupName</span></span>
<span data-ttu-id="df575-120">Anger namnet på en resurs grupp som innehåller den Traffic Manager-profil som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="df575-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df575-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df575-121">CommonParameters</span></span>
<span data-ttu-id="df575-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df575-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df575-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df575-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df575-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df575-124">INPUTS</span></span>

### <span data-ttu-id="df575-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="df575-125">None</span></span>
<span data-ttu-id="df575-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="df575-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df575-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df575-127">OUTPUTS</span></span>

### <span data-ttu-id="df575-128">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="df575-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="df575-129">Denna cmdlet returnerar ett **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="df575-129">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="df575-130">Du kan ändra det här objektet och sedan tillämpa ändringarna på Traffic Manager genom att använda **set-AzureRmTrafficManagerProfile**.</span><span class="sxs-lookup"><span data-stu-id="df575-130">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="df575-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df575-131">NOTES</span></span>

## <span data-ttu-id="df575-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df575-132">RELATED LINKS</span></span>

[<span data-ttu-id="df575-133">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="df575-133">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="df575-134">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="df575-134">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="df575-135">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="df575-135">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="df575-136">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="df575-136">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="df575-137">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="df575-137">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


