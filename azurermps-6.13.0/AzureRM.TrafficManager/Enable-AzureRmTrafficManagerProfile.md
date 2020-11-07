---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: f7ac75789e4020d3d0e645e5dac8ef2430795eb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578704"
---
# <span data-ttu-id="92e91-101">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92e91-101">Enable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="92e91-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92e91-102">SYNOPSIS</span></span>
<span data-ttu-id="92e91-103">Aktiverar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="92e91-103">Enables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92e91-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92e91-104">SYNTAX</span></span>

### <span data-ttu-id="92e91-105">Fält</span><span class="sxs-lookup"><span data-stu-id="92e91-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92e91-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="92e91-106">Object</span></span>
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92e91-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92e91-107">DESCRIPTION</span></span>
<span data-ttu-id="92e91-108">Cmdleten **Enable-AzureRmTrafficManagerProfile** aktiverar en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="92e91-108">The **Enable-AzureRmTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="92e91-109">Du kan ange profil objekt med hjälp av pipeline eller som ett parameter värde.</span><span class="sxs-lookup"><span data-stu-id="92e91-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="92e91-110">Alternativt kan du ange profilen med hjälp av parametrarna *Name* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="92e91-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="92e91-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92e91-111">EXAMPLES</span></span>

### <span data-ttu-id="92e91-112">Exempel 1: Aktivera en profil som anges med namn</span><span class="sxs-lookup"><span data-stu-id="92e91-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="92e91-113">Det här kommandot aktiverar profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="92e91-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="92e91-114">Exempel 2: Aktivera en profil med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="92e91-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

<span data-ttu-id="92e91-115">Det här kommandot får profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="92e91-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="92e91-116">Då överförs den profilen till cmdlet **Enable-AzureRmTrafficManagerProfile** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="92e91-116">The command then passes that profile to the **Enable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="92e91-117">Denna cmdlet aktiverar den profilen.</span><span class="sxs-lookup"><span data-stu-id="92e91-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="92e91-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92e91-118">PARAMETERS</span></span>

### <span data-ttu-id="92e91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e91-119">-DefaultProfile</span></span>
<span data-ttu-id="92e91-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92e91-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92e91-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="92e91-121">-Name</span></span>
<span data-ttu-id="92e91-122">Anger namnet på den Traffic Manager-profil som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="92e91-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="92e91-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e91-123">-ResourceGroupName</span></span>
<span data-ttu-id="92e91-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="92e91-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="92e91-125">Denna cmdlet aktiverar en Traffic Manager-profil i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="92e91-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="92e91-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92e91-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="92e91-127">Anger ett **TrafficManagerProfile** -objekt som ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="92e91-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="92e91-128">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="92e91-128">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92e91-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e91-129">CommonParameters</span></span>
<span data-ttu-id="92e91-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e91-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e91-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92e91-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e91-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92e91-132">INPUTS</span></span>

### <span data-ttu-id="92e91-133">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92e91-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="92e91-134">Denna cmdlet accepterar ett **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="92e91-134">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="92e91-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92e91-135">OUTPUTS</span></span>

### <span data-ttu-id="92e91-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92e91-136">System.Boolean</span></span>

## <span data-ttu-id="92e91-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92e91-137">NOTES</span></span>

## <span data-ttu-id="92e91-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92e91-138">RELATED LINKS</span></span>

[<span data-ttu-id="92e91-139">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92e91-139">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="92e91-140">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92e91-140">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="92e91-141">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92e91-141">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="92e91-142">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92e91-142">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="92e91-143">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92e91-143">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)

