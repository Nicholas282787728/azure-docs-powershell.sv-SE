---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423867"
---
# <span data-ttu-id="de0ca-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de0ca-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="de0ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de0ca-102">SYNOPSIS</span></span>
<span data-ttu-id="de0ca-103">Aktiverar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="de0ca-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="de0ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de0ca-104">SYNTAX</span></span>

### <span data-ttu-id="de0ca-105">Fält</span><span class="sxs-lookup"><span data-stu-id="de0ca-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de0ca-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="de0ca-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de0ca-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de0ca-107">DESCRIPTION</span></span>
<span data-ttu-id="de0ca-108">Cmdleten **Enable-AzTrafficManagerProfile** aktiverar en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="de0ca-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="de0ca-109">Du kan ange profil objekt med hjälp av pipeline eller som ett parameter värde.</span><span class="sxs-lookup"><span data-stu-id="de0ca-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="de0ca-110">Alternativt kan du ange profilen med hjälp av parametrarna *Name* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="de0ca-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="de0ca-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de0ca-111">EXAMPLES</span></span>

### <span data-ttu-id="de0ca-112">Exempel 1: Aktivera en profil som anges med namn</span><span class="sxs-lookup"><span data-stu-id="de0ca-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="de0ca-113">Det här kommandot aktiverar profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="de0ca-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="de0ca-114">Exempel 2: Aktivera en profil med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="de0ca-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="de0ca-115">Det här kommandot får profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="de0ca-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="de0ca-116">Då överförs den profilen till cmdlet **Enable-AzTrafficManagerProfile** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="de0ca-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="de0ca-117">Denna cmdlet aktiverar den profilen.</span><span class="sxs-lookup"><span data-stu-id="de0ca-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="de0ca-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de0ca-118">PARAMETERS</span></span>

### <span data-ttu-id="de0ca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de0ca-119">-DefaultProfile</span></span>
<span data-ttu-id="de0ca-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de0ca-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de0ca-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="de0ca-121">-Name</span></span>
<span data-ttu-id="de0ca-122">Anger namnet på den Traffic Manager-profil som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="de0ca-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="de0ca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de0ca-123">-ResourceGroupName</span></span>
<span data-ttu-id="de0ca-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="de0ca-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="de0ca-125">Denna cmdlet aktiverar en Traffic Manager-profil i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="de0ca-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="de0ca-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de0ca-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="de0ca-127">Anger ett **TrafficManagerProfile** -objekt som ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="de0ca-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="de0ca-128">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="de0ca-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="de0ca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de0ca-129">CommonParameters</span></span>
<span data-ttu-id="de0ca-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de0ca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de0ca-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de0ca-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de0ca-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de0ca-132">INPUTS</span></span>

### <span data-ttu-id="de0ca-133">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de0ca-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="de0ca-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de0ca-134">OUTPUTS</span></span>

### <span data-ttu-id="de0ca-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de0ca-135">System.Boolean</span></span>

## <span data-ttu-id="de0ca-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de0ca-136">NOTES</span></span>

## <span data-ttu-id="de0ca-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de0ca-137">RELATED LINKS</span></span>

[<span data-ttu-id="de0ca-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de0ca-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="de0ca-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de0ca-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="de0ca-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de0ca-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="de0ca-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de0ca-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="de0ca-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de0ca-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


