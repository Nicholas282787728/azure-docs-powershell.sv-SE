---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 6be04cea9e3e73a06cdbb1ee449adaefd4fe803e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757980"
---
# <span data-ttu-id="9f8a0-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9f8a0-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="9f8a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f8a0-102">SYNOPSIS</span></span>
<span data-ttu-id="9f8a0-103">Hämtar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f8a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f8a0-104">SYNTAX</span></span>

```
Get-AzureRmTrafficManagerProfile [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f8a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f8a0-105">DESCRIPTION</span></span>
<span data-ttu-id="9f8a0-106">Cmdleten **Get-AzureRmTrafficManagerProfile** hämtar en Azure Traffic Manager-profil och returnerar ett objekt som representerar den profilen.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-106">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="9f8a0-107">Ange en profil efter dess namn och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-107">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="9f8a0-108">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på profilen med hjälp av Set-AzureRmTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-108">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="9f8a0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f8a0-109">EXAMPLES</span></span>

### <span data-ttu-id="9f8a0-110">Exempel 1: skaffa en profil</span><span class="sxs-lookup"><span data-stu-id="9f8a0-110">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="9f8a0-111">Det här kommandot får profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-111">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="9f8a0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f8a0-112">PARAMETERS</span></span>

### <span data-ttu-id="9f8a0-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9f8a0-113">-Name</span></span>
<span data-ttu-id="9f8a0-114">Anger namnet på den Traffic Manager-profil som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-114">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f8a0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f8a0-115">-ResourceGroupName</span></span>
<span data-ttu-id="9f8a0-116">Anger namnet på en resurs grupp som innehåller den Traffic Manager-profil som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-116">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f8a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f8a0-117">-DefaultProfile</span></span>
<span data-ttu-id="9f8a0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f8a0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f8a0-119">CommonParameters</span></span>
<span data-ttu-id="9f8a0-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f8a0-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f8a0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f8a0-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f8a0-122">INPUTS</span></span>

## <span data-ttu-id="9f8a0-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f8a0-123">OUTPUTS</span></span>

### <span data-ttu-id="9f8a0-124">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9f8a0-124">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="9f8a0-125">Denna cmdlet returnerar ett **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-125">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="9f8a0-126">Du kan ändra det här objektet och sedan tillämpa ändringarna på Traffic Manager genom att använda **set-AzureRmTrafficManagerProfile**.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-126">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="9f8a0-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f8a0-127">NOTES</span></span>

## <span data-ttu-id="9f8a0-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f8a0-128">RELATED LINKS</span></span>

[<span data-ttu-id="9f8a0-129">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9f8a0-129">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9f8a0-130">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9f8a0-130">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9f8a0-131">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9f8a0-131">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9f8a0-132">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9f8a0-132">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9f8a0-133">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9f8a0-133">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


