---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bdfe37622db49c554f128714ab2af65a11fbfce7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580923"
---
# <span data-ttu-id="c86f6-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c86f6-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="c86f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c86f6-102">SYNOPSIS</span></span>
<span data-ttu-id="c86f6-103">Hämtar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="c86f6-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c86f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c86f6-104">SYNTAX</span></span>

```
Get-AzureRmTrafficManagerProfile [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c86f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c86f6-105">DESCRIPTION</span></span>
<span data-ttu-id="c86f6-106">Cmdleten **Get-AzureRmTrafficManagerProfile** hämtar en Azure Traffic Manager-profil och returnerar ett objekt som representerar den profilen.</span><span class="sxs-lookup"><span data-stu-id="c86f6-106">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="c86f6-107">Ange en profil efter dess namn och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="c86f6-107">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="c86f6-108">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på profilen med hjälp av Set-AzureRmTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c86f6-108">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="c86f6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c86f6-109">EXAMPLES</span></span>

### <span data-ttu-id="c86f6-110">Exempel 1: skaffa en profil</span><span class="sxs-lookup"><span data-stu-id="c86f6-110">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c86f6-111">Det här kommandot får profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c86f6-111">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="c86f6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c86f6-112">PARAMETERS</span></span>

### <span data-ttu-id="c86f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c86f6-113">-DefaultProfile</span></span>
<span data-ttu-id="c86f6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c86f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c86f6-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c86f6-115">-Name</span></span>
<span data-ttu-id="c86f6-116">Anger namnet på den Traffic Manager-profil som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="c86f6-116">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c86f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="c86f6-118">Anger namnet på en resurs grupp som innehåller den Traffic Manager-profil som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="c86f6-118">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86f6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c86f6-119">CommonParameters</span></span>
<span data-ttu-id="c86f6-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c86f6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c86f6-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c86f6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c86f6-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c86f6-122">INPUTS</span></span>

### <span data-ttu-id="c86f6-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="c86f6-123">None</span></span>
<span data-ttu-id="c86f6-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c86f6-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c86f6-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c86f6-125">OUTPUTS</span></span>

### <span data-ttu-id="c86f6-126">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c86f6-126">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="c86f6-127">Denna cmdlet returnerar ett **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c86f6-127">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="c86f6-128">Du kan ändra det här objektet och sedan tillämpa ändringarna på Traffic Manager genom att använda **set-AzureRmTrafficManagerProfile**.</span><span class="sxs-lookup"><span data-stu-id="c86f6-128">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="c86f6-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c86f6-129">NOTES</span></span>

## <span data-ttu-id="c86f6-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c86f6-130">RELATED LINKS</span></span>

[<span data-ttu-id="c86f6-131">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c86f6-131">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c86f6-132">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c86f6-132">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c86f6-133">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c86f6-133">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c86f6-134">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c86f6-134">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c86f6-135">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c86f6-135">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


